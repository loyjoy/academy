## Web push opt-in

Collect consents for Web push notifications to send personalized Web push notifications to your customers in a GDPR-compliant way.

Following requirements must be fulfilled so that the chat can ask for a Web Push opt-in:

- The Web browser must support Web push subscriptions and Web push notifications. Currently, Safari DOES NOT support Web push subscriptions! Instead, only Chrome, Edge and Firefox support Web push subscriptions. We recommend to use Google Chrome on Desktop (not on Mobile) for repeated testing.
- The hosting Web site must provide the file `service-worker.js` from tab `Publish` at the Web page root directory, e.g. at `https://www.example.org/service-worker.js`
- The customer must not have accepted or declined a Web push subscription for the hosting Web site, yet. In case of Google Chrome on Desktop this can easily checked by opening URL `chrome://settings/content/notifications` in Chrome Web browser on Desktop and checking the list of domains. Delete any existing Web push subscription for your domain, and completely RESTART Google Chrome! Only after a restart of Google Chrome you will be asked again.
- The hosting Web site must be opened with `https`, not with `http`.
- There must not be any HTTP basic authentication present on the hosting Web site, e.g. as it could be the case in a staging environment.

If these requirements are not met, the chat will simply skip the process module and proceed with the next one.
