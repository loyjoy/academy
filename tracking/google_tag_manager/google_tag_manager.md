# How to connect LoyJoy to Google Tag Manager (gtm.js)

With a LoyJoy chat on your Web site you can connect with your customers in a great way. You can watch how your customers use the chat in the LoyJoy analytics backend. Alternatively, you can integrate LoyJoy into your own website tracking solution to collect all analytics data in one place and in real-time. The tracking integration is always based on the LoyJoy [JavaScript API](/experiences/publish/javascript_api/javascript_api.md).

LoyJoy events can be pushed to Google Tag Manager via [dataLayer.push](https://developers.google.com/tag-platform/tag-manager/web) like this. Please replace all occurences of `PROCESS_ID` with you process ID:

```
<script src="https://stable.loyjoy.com/widget/PROCESS_ID"></script>
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {
    dataLayer && dataLayer.push({
      'event': evt,
      'event_category': 'LoyJoy Chat',
      'event_action': obj && obj.process_name,
      'event_label': evt + (obj.label ? '/' + obj.label : '')
    })
  }],
  process: PROCESS_ID
})
</script>
```

You can choose the fields `event`, `event_category`, `event_action` and `event_label` freely and/or add other fields when optimizing events for Google Tag Manager. The aforementioned fields intentionally resemble the fields for Google Analytics 4, in case that Google Analytics 4 is the primary analytics platform configured behind Google Tag Manager.


## Filter for specific LoyJoy events

The LoyJoy JavaScript API will emit a large list of [events](/experiences/events/events.md) and thus possibly generate a lot of events in Google Tag Manager. LoyJoy events can be filtered to a subset such as `['load', 'open', 'start', 'session_started', 'interaction']` like this. Please replace all occurences of `PROCESS_ID` with you process ID:

```
<script src="https://stable.loyjoy.com/widget/PROCESS_ID"></script>
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {
    if (['load', 'open', 'start', 'session_started', 'interaction'].includes(evt)) {
      dataLayer && dataLayer.push({
        'event': evt,
        'event_category': 'LoyJoy Chat',
        'event_action': obj && obj.process_name,
        'event_label': evt + (obj.label ? '/' + obj.label : '')
      })
    }
  }],
  process: PROCESS_ID
})
</script>
```


## Example 1

The following snippet is an example for a tenant, which only wanted to send specific customer interactions from the chat to Google Tag Manager. Please replace all occurences of `PROCESS_ID` with you process ID:

```
<script src="https://stable.loyjoy.com/widget/PROCESS_ID"></script>
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {
    if ([
      'data_collection_question_answered', 'interaction', 'link_clicked', 'load', 'open', 'session_started', 'session_interacted', 'start',
      'jump_decision_1', 'jump_decision_2', 'jump_decision_3', 'jump_decision_4', 'jump_decision_5', 'jump_decision_6', 'jump_decision_7',
      'jump_persistent_1', 'jump_persistent_2', 'jump_persistent_3', 'jump_persistent_4', 'jump_persistent_5'      
    ].includes(evt)) {
      dataLayer && dataLayer.push({
        'event': 'LoyJoy ChatBot ' + evt,
        'event_category': 'LoyJoy ChatBot',
        'event_action': ['load', 'session_started', 'session_interacted'].includes(evt) ? evt : obj && (obj.process_name || obj.process_id),
        'event_label': ['load', 'session_started', 'session_interacted'].includes(evt) ? evt : evt + ' / ' + (obj && obj.label ? obj.label + ' / ' : '') + (obj && obj.sub_process_name ? obj.sub_process_name + ' / ' : '')
      })
    }
  }],
  process: PROCESS_ID
})
</script>
```
