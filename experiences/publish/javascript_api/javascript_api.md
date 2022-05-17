# Manage LoyJoy Website Integration with JavaScript API

The LoyJoy JavaScript API is a powerful programming interface to control the LoyJoy chat on your website and to personalize the content of your website. The API allows you to show and hide the LoyJoy chat bubble, open and close the chat window, and much more. The events triggered by LoyJoy allow you to react to the chat events, for example using the name entered by the user to address him personally. You can also use LoyJoy as an authentication provider by having your users sign into the chat and then relying on the user data provided by LoyJoy.


## Script integration

The script integration registers the global function `LoyJoy` in the DOM `window` object. It does not change other parts of the DOM. PROCESS_ID must be replaced with your own ID from the LoyJoy manager.

```html
<script src="https://cloud.loyjoy.com/widget/PROCESS_ID"></script>
```

## Render the chat as an overlay on your Web page

Injects LoyJoy DOM elements into the DOM and shows the chat bubble as configured in the LoyJoy manager.

```html
<script>
LoyJoy('boot', {
  process: PROCESS_ID
})
</script>
```

## Render the chat into a div layer on your Web page

Injects LoyJoy DOM elements into the DOM and renders the messenger into a div with the id `loyjoy-chat`. The div size can be modified freely.

```html
<div id="loyjoy-chat" style="width: 376px; height: 600px; line-height: 0; padding: 0"></div>
<script>
LoyJoy('boot', {
  process: PROCESS_ID
})
</script>
```

## Open

Opens the LoyJoy chat. Opposite to close.

```html
<script>LoyJoy('open')</script>
```

## Close

Closes the LoyJoy chat. Opposite to open.

```html
<script>LoyJoy('close')</script>
```

## Remove

Removes the LoyJoy DOM elements from the DOM.

```html
<script>LoyJoy('remove')</script>
```

## Hide

Hides the LoyJoy element in DOM (display: none), but does not remove it. Opposite to show.

```html
<script>LoyJoy('hide')</script>
```

## Show

Makes the LoyJoy element visible in DOM. Opposite to hide.

```html
<script>LoyJoy('show')</script>
```

## Locale

A string in the format `<language-iso-6391>_<region-iso-31662>` (two-letter-codes) overwrites the user’s settings regarding language and region. This language and region will be saved as the customer’s language and region.

```html
<script>
LoyJoy('boot', {
  locale: 'en_US',
  process: PROCESS_ID
})
</script>
```

## Restart

Tells the chat to restart the process after (1) a page reload, (2) calling `LoyJoy('boot')` or (3) jumping to another experience. This removes the chat history and restarts the experience from the beginning. In contrast to `reset` the session remains intact, i.e. the customer remains signed in and variables are not removed.

```html
<script>
LoyJoy('boot', {
  process: PROCESS_ID,
  restart: true
})
</script>
```

## Reset

Tells the chat to reset the process after a page reload (or after a new `LoyJoy('boot')`). This removes the chat history and restarts the experience from the beginning.

```html
<script>
LoyJoy('boot', {
  process: PROCESS_ID,
  reset: true
})
</script>
```

## Open

Tells the chat to open the messenger window independent of other configuration settings.

```html
<script>
LoyJoy('boot', {
  open: true,
  process: PROCESS_ID
})
</script>
```

## Cookie consent

A callback function, which signals cookie consent, e.g. from a cookie consent bar on the hosting website.

```html
<script>
LoyJoy('boot', {
  cookieConsent: function () {
    return true
    // e.g. return ('; ' + document.cookie).split('; ' + 'MarketingCookiesEnabled' + '=').pop().split(';').shift() == '1'
  },
  process: PROCESS_ID
})
</script>
```

## Events

The chat emits events for chat events (open, close, sign-up, etc.) that can be registered for with event listeners. 

```html
<script>
LoyJoy('boot', {
  eventListeners: [function (evt, obj) {}],
  process: PROCESS_ID
})
</script>
```

## Freely selected parameters

Passes freely selected parameters to the experience that can be evaluated in the BPMN process using BPMN conditions and other expressions. For example, the parameters can be accessed with the `GetParam` function in LoyJoy.

```html
<script>
LoyJoy('boot', {
  params: {
    foo: 'bar'
  },
  process: PROCESS_ID
})
</script>
```

### Callback parameters

Similar to freely selected parameters you can supply a callback function that will be evaluated dynamically. The callback also results in a parameter that can be used in the BPMN process via `GetParam`.

```html
<script>
LoyJoy('boot', {
  callbacks: {
    foo: () => window.location.href
  },
  process: PROCESS_ID
})
</script>
```

## Disable service worker

By default LoyJoy will try to load the service worker from `/service-worker.js` to enable e.g. push notifications. To prevent LoyJoy from trying to load the service worker you can use the parameter `serviceWorkerDisable`. This is useful, if there is no `/service-worker.js` present and you want to prevent a `HTTP 404` error.

```html
<script>
LoyJoy('boot', {
  process: PROCESS_ID,
  serviceWorkerDisable: true
})
</script>
```
