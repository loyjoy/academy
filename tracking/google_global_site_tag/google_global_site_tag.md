# How to connect LoyJoy to Google Global Site Tag / Google Analytics (gtag.js)

With a LoyJoy chat on your Web site you can connect with your customers in a great way. You can watch how your customers use the chat in the LoyJoy analytics backend. Alternatively, you can integrate LoyJoy into your own website tracking solution to collect all analytics data in one place and in real-time. The tracking integration is always based on the LoyJoy [JavaScript API](/experiences/publish/javascript_api/javascript_api.md).

LoyJoy events can be pushed directly to Google Analytics 4 via [gtag.js](https://developers.google.com/tag-platform/gtagjs) like this. Please replace all occurences of `PROCESS_ID` with you process ID:

```
<script src="https://stable.loyjoy.com/widget/PROCESS_ID"></script>
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {
    gtag && gtag('event', evt, {
      'event_category': 'LoyJoy Chat',
      'event_action': obj && obj.process_name,
      'event_label': evt + '/' + (obj.label ? obj.label + '/' : '')
    })
  }],
  process: PROCESS_ID
})
</script>
```

You can choose the fields `event_category`, `event_label` and `value` freely when optimizing events for Google Analytics 4, as also described in [Measure Google Analytics Events](https://developers.google.com/analytics/devguides/collection/gtagjs/events).


## Filter for specific LoyJoy events

The LoyJoy JavaScript API will emit a large list of [events](/experiences/events/events.md) and thus possibly generate a lot of events in Google Analytics. LoyJoy events can be filtered to a subset such as `['load', 'open', 'start', 'session_started', 'interaction']` like this. Please replace all occurences of `PROCESS_ID` with you process ID:

```
<script src="https://stable.loyjoy.com/widget/PROCESS_ID"></script>
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {
    if (['load', 'open', 'start', 'session_started', 'interaction'].includes(evt)) {
      gtag && gtag('event', evt, {
        'event_category': 'LoyJoy Chat',
        'event_action': obj && obj.process_name,
        'event_label': evt + '/' + (obj.label ? obj.label + '/' : '')
      })
    }
  }],
  process: PROCESS_ID
})
</script>
```
