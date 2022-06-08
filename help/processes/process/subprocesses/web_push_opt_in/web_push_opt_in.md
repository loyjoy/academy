## Web push opt-in

Collect consents for Web push notifications to send personalized Web push notifications to your customers in a GDPR-compliant way.

Following requirements must be fulfilled so that the chat asks for a Web Push opt-in.

- The Web browser must support Web push subscriptions and Web push notifications. Currently, Safari does not support Web push subscriptions! Instead, only Chrome, Edge and Firefox support Web push subscriptions.
- The hosting Web site must provide the file `server-worker.js` from tab `Publish` at the Web page root directory, e.g. at `https://www.example.org/service-worker.js`
- The hosting Web site must be opened with `https`, not with `http`.
- There must not be any HTTP basic authentication present on the hosting Web site, e.g. as it could be the case in a staging environment.
- The customer must not have accepted or declined a Web push subscription for the hosting Web site. In case of Chrome this can easily checked at [Notification Settings](chrome://settings/content/notifications).
