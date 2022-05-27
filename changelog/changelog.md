
# Change Log

All notable updates and changes to the LoyJoy Cloud are documented here.


### Process Modules

- Process module `Pdf`
  - It is now possible to add file attachments to emails
- Process module `Send Email`
  - It is now possible to add file attachments to emails
- Process module `Variable`
  - It is now possible to set multiple variables
- Process module `Welcome`
  - Recurrent users are now greeted differently


### Platform
- Sessions
  - The expiry time of a session can now be adjusted in the branding tab of an experience
- Entity storage time
  - The expiry time of relevant entities after which entities are deleted can now be configured
- Impressum and Privacy
  - These options are now available to be shown in the navigation bar
- NLU
  - It is now transparent which intents were edited since the last training
- Analytics
  - The amount of total answers for decision jump will now be shown

### Fixes
- Persistent quickreplies are now hidden when the user enters the live chat
- When a form-based question has been asked, clicking on a persistent quickreply will no longer treated as an answer
- Products in the product selection of the shopify module can now be add to the cart although the chat is no longer in the shopify module
- A bug was fixed that caused the DMN to evaluate the rules incorrectly
 
## release-2022-05-12

### Added

- Added process module `Lottie` for Lottie background animations.
- In chat bubbles and chat forms now line breaks are enforced in case of too long texts.


## release-2022-05-10

### Added

- Process module `Snapshot` does not overwrite existing snapshots in case of repeated snapshots, but instead stores a snapshot history.
- Process module `ApiClient` writes variable `api_client_status_code` containing the HTTP status code.


## release-2022-04-30

### Added

#### Process Modules

- Process module `Handover`
  - The user request can now be made obligatory
- Process module `Live`
  - The user request in asynchronous answers can now be made obligatory
- Process module `Prizes`
  - A prize can now be expanded instead of indirectly asking through the "More" Button on details regarding that prize

#### Platform

- Live
  - The live chat now displays the user answers provide in a form. E.g. Email or postal address
  - Notifications are played up to three times if an agent has not given an answer
  - Notifications are played only when the agent is inactive, switches browser tab or works in a different app
- Variables
  - New function: `Formatted Date Today`. Evaluate the localized date of today in conditions or store it as variables
  - New function: `Formatted Date Tomorrow`. Evaluate the localized date of tomorrow in conditions or store it as variables

### Fixed

- A problem is fixed that causes the live chat to end too early


## release-2022-04-22

### Added

- Process module `Handover`
  - Transition from assignments determined by quiz answers to assignments determined by expressions.


## release-2022-04-20

### Added

#### Process modules

- New process module `OneTrust` integration
  - Create or update consent receipts in OneTrust.
  - Retrieve existing consent receipts from OneTrust.
- New process module `JavaScript`
  - Allows you to execute arbitrary JavaScript code in the user’s browser
  - Results can be set as variables
- New Process Module `PDF` 📄
  - Generate a PDF from a HTML template and populate user information using variables
  - Either offer it for download directly in the chat...
  - ... and/or send the PDF via email to the customer and/or to a specified set of emails
- New Process Module `Jump to home view`
  - If a home view is configured this process module jumps to it.

#### Platform

- Added bulk operations for multiple experiences
  - Move, archive, and pause multiple experiences simultaneously.
  - Paste the branding of one experience into muliple experiences simultaneously.
- Images in the image gallery are now zoomable
- Process module `NPS`
  - Switch between emoji slider and numbers slider.
- BPMN Connectors - Google sheets
  - Connect your data in Google Sheets with LoyJoy modules. Currently available for the places module.
- 📈 Analytics
  - Analytics for NLU models
  - Analytics for persistent jump quick replies
- 💬 Live chat
  - The current experience of the user is now shown in the sidebar
  - Added an analytics event for live chat requests missed by an agent
  - The agent can now add a display name, role, and a personalized welcome message
  - ... together with the agent's avatar these are sent to the customer for greeting
  - A notification is now played when the agent switches tabs and a new conversation arrives or a new message of the current conversation comes in
  - Default waiting time is now increased to 120 seconds
- Process module `birthdate`
  - Minimum age can now be checked automatically based on the current date
- Questionnaire process module
  - The question type `NPS` now enables NPS score calculation in the analytics
  - It is now possible to edit the variable value for the skip button
  - The default value of the variable was changed to `skip`
- Add check for regular expression for email input
- Shopify OAuth
  - Integrate LoyJoy into your shopify store with a few clicks thanks to OAuth
- Design your chat
  - Change the appearance of your chat like colors and border colors for each item individually
  - Use your own font and give the chat your own visual touch
- NLU Evaluation
  - While evaluating NLU messages an intermediary step is now necessary to assign messages to intents
  - When adding messages to intents, the text can be modified beforehand
- Chat preview now collects data about
  - Messages shown
  - Message clicked
  - Quick replies shown
  - Quick reply clicked


### Updated

- New send icon ➡️
- Search 🔎
  - By default the user input below the chat is now a search input field.
  - Let your user search your experiences and let them start experiences on their own
  - To make an experience searchable, make sure you provide a title and a description for the experience
- UX
  - Experiences are now grouped by folders while selecting e.g. in jumps
  - Copy text IDs on click in texts table
  - Improved decision table presentation (show function arguments, show spaces)
  - Improve fixed value expression input (no enter to confirm, warn if padded with whitespace)
- Places/Address query
  - Redesigned autocomplete
- The chat preview has been updated visually
- PIN / Code input field is not type password

### Fixed

- Fixed swipe behaviour in carousels for safari
- Fixed performance issues in template store


## release-2022-03-14

### Added

- New Process Module `Places` 📍
  - Ask your customers for their address and calculate the distances to a set of locations. Show the closest 4 locations as a list and offer direct navigation.


## release-2022-02-28

### Added

- New API client module
- Assets are now delivered from a CDN
- Added OpenTelemetry for continuous performance analysis
- Image gallery images can now be rendered with orientation `landscape`, `square` or `portrait`.


## release-2022-02-07

### Added

- 📁 Grouping of experiences
  - Process groups are now identified by their creation date, the identifier can be edited in the process group view.
  - Customize the process group of an experience using the popover in the process edit menu.
- 🗂️ Archiving of experiences
  - Experiences now have one of the following states: active (default), suspended, archived.
  - Archive experiences via the respective popover in the process list view.
  - Experiences with state archived behave like experiences with state inactive, furthermore they are hidden in the process list view by default.
  - Show all archived experiences of a group by toggling the respective popover in the process group view.
- Moved management of home views to experience
  - To add a home view to an experience select the desired one in the leave button (<) of the branding tab in the experience view
- Copy branding
  - Copy the branding of an existing process into the current process.
  - All current brand attributes are lost in this process.
  - The process from which the copy was made is displayed along with the date of the operation.
  - The copied assets are stored separately, changing the branding attributes of the process that was copied from will not affect the copied branding attributes.
- Template store
  - Prefilled Templates got a whole rework. Create prefilled experiences with ease and joy.
  - In addition, you can subscribe to templates of other tenants. This allows for simple sharing of your curated processes with other tenants.
- New `data` view replaces old `customers` view. 
  - All tables are presented with their expiry duration.
  - Role `editor` can view anonymized customer data.
- 🎊 New animations: Magenta confetti, magenta snowflake, golden raining stars.
- Inxmail integration
  - Subscription and unsubscription of customers to mail listings via inxmail.
- 🛒 Shopify OAuth-Flow
  - Integrate LoyJoy into your shopify store with few clicks.
- Process module `Code`
  - Codes are now entered into a form, not into the footer text input.
- 📈 Analytics
  - Sign-in module shows number of correct and incorrect code entries.
  - Questionnaire shows advanced data for NPS questions
  - Add count of connected API errors over time in overview and drilldown
- 💬 Live chat
  - If the chat is not in the current tab, the customer now receives an audio notification on new messages
  - Additional information like current website, referral and user agent of the customer are now displayed right next to the chat
- 🗣️ NLU
  - The management of intents are now entirely decoupled from bots respectively experiences
  - In order to use NLU in an experience, create a *Model* in the NLU section with a certain language
  - Create and maintain intents for different models separately 
  - To make a *Model* available for an experience, select it in the free text input of the branding tab in the experience view
  - Redesigned the procedure for the approval of NLU messages.
  - New NLU engine based on RASA open source
- 🖼️ Image buttons
  - Download (new) and delete (change) button
- Participation module
  - Add `participated_at` column for selected random participants
- 📜 Log
  - Split the log for manager and runtime. The runtime log is purged every 7 days.
- 🏛️ ChatUi
  - All inserted links sent to the customer are now clickable
- ℹ️ Reworked Help-Sidebar

### Fixed

- Outdated users
  - User confirmation emails are no longer sent twice.
- Analytics
  - Various small fixes for graph labels

### Removed

- ❓ Quiz
  - Freetext answer options were removed


## release-2021-11-04

### Added

- Extended chat preview features
  - Adaptive display duration and delay 
  - Up to 3 quick-replies: Experience jump in bot, experience or sub-process jump in experience
- Live chat
  - By hovering over the agents online indicator it now shows a list of all agents who are online
  - A sound will now only be played when the new conversation is live
  - An indicator at the conversation now shows the conversation origin of the sound
- The chat messenger UI can now be placed in the flow of the hosting Web page by adding a container element such as `<div id="loyjoy-chat" style="width: 600px; height: 500px"/>` before the LoyJoy JavaScript snippet. This is an alternative to the default chat UI with position fixed, which by default overlays the hosting web page.
- Added data model for Stripe integration.


## release-2021-10-25

### Added

- 📈 Analytics
  - Added a table showing the number of starts for each process.
- Removed requirement for customer database in all process modules
  - Process module `Email` can be used instead of process module `Sign-in` for all process modules, which before required a sign-up.
  - E.g. if customer database is disabled, process module `Sign-in` still works, which was not possible before.
  - This enables LoyJoy to run completely without a database.

### Fixed

- Live chat
  - It is now not longer possible to end chats twice when filtering the conversations for live chats.


## release-2021-10-11

### Added

- Image size recommendations
  - Recommendations for the best image size were added to every image upload.
  - Warning when uploading an image and animated GIF which exceeds the recommended file size.
  - Displays warning when the currently uploaded image or animated GIF exceeds the recommended file size.
- Add training data for NLU from customer messages
  - Messages from chats can now be assigned to intent training data to extend the training data.
- Live chat
  - It is now possible to filter solely for live chats.
  - You can now end the live chat with one button click.
  - Whenever you route your customer to other processes or process modules the destination is now shown in the chat.
  - Message templates can now be edited before sending.
  - A typing indicator gives your users feedback on whether their request is being processed.
  - An online indicator provides information to the agent whether the user is still in the chat.
  - When no agent is online or no agent responds, the user can now leave a message and provide an email addresse for response notifications.
  - It is now not longer necessary to select the responsible agents inside the process module. An agent therefore only needs to set her/his online state in the live view.
- 📈 Analytics:
  - Home view
    - From now on every click in the home view are being counted and provided in analytics.
  - `List` process module
    - From now on every click on a element is being counted and provided in analytics.
- New function: `User agent`
  - Returns the customer's user agent
- E-Mail addresses are added to `code` & `coupon code` CSV downloads for redeemed codes


## release-2021-09-29

### Added

- New Process module: `Email`
  - Ask your customers for their email address.
- Refactored process module `Timer`.
  - Timer settings are now self-explaining in the manager
  - Timers are executed with second-precision
- Added new function `IsoLocalDateTime`.
- The z-index of bots and processes can now be edited.
- Animations between Chat UI view are now smoother due to CSS only instead of JavaScript.


## release-2021-09-07

### Added

- New modes for the `Salesforce Marketing Cloud` process module:
  - Assure contact
  - Send email
- New functions `newsletter_double_opt_in_url` & `profiling_double_opt_in_url` can be used to create opt-in URLs e.g. in mappings

### Changed

- Several process modules no longer require a previous sign-in: `Web-push opt-in`, `Notification`, `Reminder`. Instead these now solely rely on push subscriptions, which are anonymous by default.

### Fixed

- Fairy dust animation color
- Loyalty coin image can be added for bots (hidden setting)


## release-2021-08-26

### Added

- Integrate your Shopify store in LoyJoy with the brand new process module `Shopify` 🛍️
  - Display and filter products of your Shopify store in the chat.
  - Add items to the Shopify cart within the chat. 🛒
  - View the current shopping cart in the chat and let your customers modify it.
- New process module `Jump return`. This is useful for reusing experiences in other experiences like a function call. Jump into a called process and after ending  automatically return to the calling process. 
- Process module `Questionnaire` now offers the beloved emoji slider as known from the `NPS` process module. 😍
- Process module `Postal address` now optionally asks for a country which can be selected from a list of predefined options. This feature can be activated by adding countries in the process module.
- Process module `Live` now distinguishes between `Waiting for agent` and `Live chat started`.
- By default LoyJoy loads the service worker from /service-worker.js to enable e.g. push notifications. To prevent LoyJoy from trying to load the service worker you now can use the parameter `serviceWorkerDisable: true` to prevent an HTTP 404 error.
- Added several modes to process module `Beiersdorf`.

### Changed

- Removed support for Internet Explorer 11. In case of Internet Explorer 11 the chat does not render anymore. 👋
- Carousels now do not render a scroll bar anymore. This is possible due to removal of support for Internet Explorer 11.
- Several process modules no longer require a previous sign-in: `Code`, `Coupon code`, `Loyalty`, `Loyalty referral`, `Loyalty sharing`, `Giveaway participation`, `Instant win`. Instead these simply require an `auth_email` variable to operate, which is set by other process modules such as `Sign in`, `ReachFive` or `ProCampaign`.
- Stories style for `compact` and `large` has been simplified to `large` only. Thus, stories now always have a cover and optionally an avatar.
- Removed process module `In-chat push`.

### Fixed

- Fixed color of the Fairy Dust animation. ✨
- Fixes in icon view for questionnaire single choice and multiple choice questions.


## release-2021-08-17

### Added

- Added process module `Opt-ins`, which shows all opt-ins of a customer with the option to opt out. Before this was a hard-coded part of the settings area.
- Added process module `Edit email`, which allows the customer to change the email address. Before this was a hard-coded part of the settings area.
- Several process modules no longer require a previous sign-in: `Notification`, `Process Instance List`, `Reminder`.
- Process modules `Participation` and `Loyalty` now check terms autonomously without requiring a `Sign-in` process module in the same experience.
- JavaScript API parameter `restart` now restarts on (1) a page reload, (2) calling `LoyJoy('boot')` or (3) jumping to another experience.


## release-2021-08-12

### Added

- 📈 New Analytics
  - New detail view with heat map: Allows to display the performance per process module.
  - New session concept: Chat opens & interactions within 30 minutes are measured.
  - New, bot-wide analytics with aggregated performance measurement.
- Copy function for process modules
  - Functionality to specify the position at which a copied process module should be pasted.
- Updated process module `Questionnaire`
  - Questionnaire result email is obsolete and going to be removed soon. Until then, it will inform about the planned removal.
- Updated process module `Search`
  - Search queries can now be entered in a form in the chat instead in the text.
- All opt-ins such as newsletter opt-ins are now stored primarily as customer variables. As such they can be read and written with their variable name such as `customer_newsletter_single_opt_in`. When writing a variable such as `customer_newsletter_single_opt_in = true` in a process, in the background the corresponding row in the `opt-ins` table is automatically written for later CSV export of opt-ins.
- Several process modules no longer require a previous sign-in: `Newsletter opt-in`, `Profiling opt-in`, `Reminder opt-in`, `Web push opt-in`, `Text message opt-in`. Instead these simply require an `auth_email` variable to operate, which is set by other process modules such as `Sign-In`, `ReachFive` or `ProCampaign`.
- Live
  - As a live agent you are now able to create message templates for the live chat. With one click you can send predefined messages and answers for recurring user requests.
  - You are now able to block users for 48 hours.


### Fixed

- Prevent customers from entering only spaces in forms such as first name, phone number, and questionnaire forms.
- List jumps now work correctly if previously jumped to from another process.


## release-2021-08-02

### Changed

- Process module `ReachFive` now implements authentication server-side instead of client-side.

### Fixed

- Fixed potentially negative width of elements in data collection question type `Rating`.


## release-2021-07-27

### Added

- Process Editor View features a new process module palette
  - Process modules are categorized by topic such as `loyalty` or `integration`. The categories are ordered by priority, starting with the most basic process modules.
  - Process modules can be filtered and searched by name, group name, tags.
  - The palette can be switchted to fullscreen view to show process module previews.
- Updated jump logic in process modules such as `Decision Jump` and `Automatic Jump` as well as intents.
  - You can now optionally open a new chat view when jumping to another experience. This enables to visually jump between experiences with a smooth transition.
- Find any text instantly: New global search in manager 🔎
  - Search for any text in any experience and go to the exact location with ease.
- New process module `Search` 🔎
  - Lets your customers search through your whole bot. On success, the chat jumps into the experience found.
- New Home View Widget `Search` 🔎
  - Let your customers enter a search query and suggest experiences to jump into.
- Updated process module `External Link`
  - Links can now be embedded in the ChatUI for the following content providers: *codepen, kickstarter, mixcloud, nytimes, pinterest, soundcloud, spotify, ted, vimeo, youtube*
- Several process modules do not require a sign-in before: `Firstname`, `Lastname`, `Gender`, `Birthdate`, `Phone`, `Postal Address`, `Tags`, `Personal Data Intro`. Instead they simply create customer variables such as `customer_firstname`, which additionally automatically is written to the Vault, as soon as the customer is signed in. Thus, using the Vault is now optional.
- Several process modules do not trigger a sign-in before: `Mail to Customer`, `InChat Push`, `Rewards`, `Scondoo`, `Yotpo`. Instead these simply require an `auth_email` variable to operate, which is set by other process modules such as `Sign-In`, `ReachFive` or `ProCampaign`.
- Process module `WebService` and `WebComponent` params can now hold expressions.
- Process module `WebComponents` can now write variables.
- Date-specific texts have now a deletion option in LoyJoy manager

### Fixed

- Blocking of autocomplete for credentials in manager
- Add suggested image sizes for image uploads
- Data collection question types `Categorical Slider` and `Rating` are now more robust, especially on rendering the chat history after page reload.


## release-2021-06-30

### Added

- Widgets in Home View are now hidden if they do not contain content
- New process module `Salesforce Interaction Studio`
- Web components are now available inside the chatflow
- Web components can now be used in footer of ChatUI
- Web components can now be parameterized
- Notifications in the Home View notifications widget are now stacked if more than one
- Live chat messages are now stored either in database or in-memory. In-memory is for financial institution tenants such as banks, database for other tenants.

### Fixed

- Fixed a bug that caused Web components to be included only once


## release-2021-06-16

### Added

- 📈 Analytics
  - New events are counted
    - Customer data entered (birthdate, name, ...; cf. [screenshot](changelog/2021-06-07-customer_data.png))
    - Opt-in rejected (cf. [screenshot](changelog/2021-06-07-opt_in_rejected.png))
    - Auto-jump (cf. [screenshot](changelog/2021-06-07-automatic_jump.png))
    - Questionnaire question answered (cf. [screenshot](changelog/2021-06-07-questionnaire.png))
    - Mail sent (cf. [screenshot](changelog/2021-06-07-email.png))
    - Proceed confirmed (cf. [screenshot](changelog/2021-06-07-proceed.png))
    - Intent matching (cf. [screenshot](changelog/2021-06-07-intents.png))
  - Heatmap showing how many of certain process blocks are reached (cf. [screenshot](changelog/2021-06-07-heatmap.png))
  - Optimizations
- List process brick
  - Added jump functionality to elements
- ChatUI
  - Inverted colors of header: The header of new processes has now a white background and the font color is the primary color
  - However, this can be inverted back to the traditional design under the `branding`-tab
  - Increased size of the header-title
- Audio recording
  - Customers can record and send an Audio in the Chat. (Not supported in `ie11`)
  - If the customer is logged in, the Audio will be saved in the history.
- Audio player: depending on the browser the following functionality is available
  - display of audio duration and progressbar (not supoprted in `safari`)
  - jump forwards and backwards in current playtime (`firefox`(all files), `chrome, edge-chromium, ie11`(for files approx. smaller than 3 MB), not supported in `safari`

### Fixed
- Questionnaire:
  - Placeholder for numerical inputs is now editable
- Image Gallery:
  - Indicator of the active item has color
- Added auto translation on bot level


## release-2021-05-25

### Added

- `External link` process module
  - Titles, descriptions and images are now loaded automatically based on og-tags of respective website
  - Link clicks are measured and displayed in analytics.
- `List process` module
  - List elements can now be conditioned
- `Mini program` process module
  - Can now be opened automatically
  - Footer for closing the mini program can now be hidden
  - An optional clickable teaser image can now be added
- `Notification` module
  - Notifications can now be sent via SMS with help of Twilio.
  - For this to work, customer must have given an SMS opt-in with `SMS opt-in` module and entered their phone number with `Phone number` module.
- `Product` module
  - Link clicks are measured and displayed in analytics.
- `Timer` process module
  - It is now possible to add absolute start and end dates
- 📈 Analytics
  - Process starts are measured and shown in analytics.
  - Link clicks are measured in the `External link` and `Product` modules.
- Callbacks added to JavaScript API
- Text inside draggable components is now selectable
- All CSV exports are provided as encrypted ZIP files

### Fixed

- `List` process module
  - Margin of elements while solely using titles


## release-2021-05-10

### Added

- `SMS opt-in` process module now supports Twilio
- Chat "send message" button icon can now be adjusted via image upload in branding.
- 📅 `Appointment` process module: Option to add a lead time
- 📈 Analytics
  - Analytics for decision jump process module
  - Analytics for live chats
  - Analytics for home view
- Policy user add
  - suitable greeting, if no first name known
  - new welcome email to the added user
- Animations
  - New animations: Autumn Leaves, Santa, Cheese, Christmas balls, Easter eggs, Gift boxes, Pine cones, Pumpkins, Raining stars
  - Animation subprocess
- `Questionnaire` process module
  - new question type: email

### Fixed

- Stochastic timeout on image upload in Firefox Android
- BPMN variable select popover
  - Underlying dialog no longer closes on any click
  - Resize to fit to screen


## release-2021-04-13

### Added

- `Mail` process module can now send attachments
- Added `Clipboard` process module
  - Show a text that your customers can copy


## release-2021-03-29

### Added

- New help bar on the right of LoyJoy manager with context information for all functionalities of LoyJoy.
- New Process module `List`
  - Show a list of generic elements to your customers and let them optionally react on it
- New process module `Salesforce Service Cloud`
- New process module `Clever Reach`
- In branding added option to disable `Restart chat`
- In branding added option to enable `Reset chat`
- In branding added option for fullscreen mode.
- Added event bus for ChatUI. When emitting event `route_home` with event process module, the ChatUI changes to home view.
- In process module `Appointment` added option to send event description via email as password encrypted PDF attachment.
- All surrounding micro-services for data storage etc. now can be disabled by super admins, allowing the LoyJoy runtime to be executed in-memory only, thus enabling the deployment of the LoyJoy runtime as an appliance in environments without any storage capabilities (e.g. embedded devices).


## release-2021-03-23

### Added

- New process module `Campaign Monitor`
- New process module `Scondoo`
- New process module `Google Pub/Sub`


## release-2021-03-22

### Added

- New process module `Password`
  - Ask your customers for a password which is stored encrypted in the session


## release-2021-03-19

### Added

- Radically simplified `ProCampaign` process module. Everything now is managed in the process module, not in the integration.


## release-2021-03-18

### Added

- User accounts can now be added to multiple tenants.
  - Simply add the user email address to multiple tenants in the tenant settings.
  - After sign in, the user can select a tenant with the tenant select control on top right beside the LoyJoy logo.


## release-2021-03-12

### Added

- Extended capability for locale `ar`. Also markdown can now be used everywhere in the chat UI.
- New analytics connector for pushing analytics fact and dimension table to BigQuery.
- Introduced Web components to enable 100% customization of home screen and chat bubbles, also by 3rd-party developers. With this release custom splash screen and home view widgets are possible, custom chat bubbles will follow.
- `Video` process modules now can autoplay the first video.

### Fixed

- Fixed seeding standard NLU intents, which where seeded multiple times before depending on the number of locales active on the bot.


## release-2021-03-04

### Added

- Added process module `Reset` for resetting the complete session, not only changing the process instance.


## release-2021-03-03

### Added

- Added Function `IsMobile` to check, if the customer is chatting from a mobile device.
- The imprint is only offered in the chatbot navigation bar, if it is configured.
- Chat UI
  - The chat can now have an avatar image, representing the bot/live agent.
- `Data collection` process module
  - Option to allow dynamic loading of dropdown options
- `Product` process module
  - Button to set variable
- `Phone number` process module
  - Similar to first name and last name now the phone number of the customer can be collected in the chat.
- `SMS opt-in` process module
  - Added process module to collect SMS opt-ins for phone numbers
- Birth date, first name, last name, phone number, gender, postal address can now be reasked, e.g. for building a customer settings chat process. These values before were only asked once.


## release-2021-02-17

### Added

- The local storage is now used tenant-wide, not bot-wide. Thus, the authentication context of a bot is shared with the other bots of that tenant, inducing less sign-ins for the customers.
- Added variable `loyalty_balance`, containing the loyalty point balance for a customer
- Added a new function `customer_age`.
- Separated storage for customer variables and process variables into a long-term storage and a transient store for more fine-granular control over variable life cycles.
- In the chat UI texts are now interpolated in the client, not on the server, enabling a more responsive reaction on variable changes in the UI.
- In case of a LoyJoy update the manager and chat now asks for a browser reload.


## release-2021-01-28

### Added

- `ProCampaign` process module: replaced hardcoded configuration properties for consent text and list
  - consent text is modeled in a mapping as `<consent text key> := Function I18nTranslate(<i18n_key as copied from texts table>)`
  - list is modeled in a mapping as `<list key> := 1`
- Sub processes can now be copied in the process editor


## release-2021-01-26

### Added

- Chat UI
  - Added option to disable user input field
  - Added option to lock process from modifications 🔒
- Redesigned the branding tab in manager
  - Branding now only contains options for styling the chat UI (i.e. no texts/content elements)
  - The branding can be inherited from the bot. This is practical for bots with many processes, which should have the same styling.
  - Some former branding settings such as SMTP settings, persistence quick replies and timezone now are configured below the list of process modules or in the respective process module
- Extended Live chat capabilities
  - Animation payload indicator in live view
  - Live view redesign
  - Splitted live and bot message sessions with tabs
  - Notifications with mute button
  - Added Emoji picker
  - Switch for agents being online/offline
  - Option for fallback stratgy if agent does not reply


## release-2021-01-15

### Added

- Process module `Sign In` now triggers the sign in chat flow.
- Variables now have a store (Browser, Server) and scope (process-specific, process-independent).
- `Live` process module: Agents configuration
  - Agents can now be defined on a `Live` process module.
  - Agents can declare themselves as online/offline in live view.
  - If there are no agents online when a user enters the `Live` process module, the process module is skipped.


## release-2021-01-11

### Added

- Upload option for BPMN XML files of bots and processes
- Intents additionally are matched rule-based against intent training data
- Added REST endpoints for programmatically downloading XML process definitions
- Added debug mode in manager that makes internal chat mechanics transparent


## release-2021-01-07

### Added

- New process module: `Appointment` 📅
  - You can use this module to let your customers schedule invididual appointments.
  - Appointments are stored as iCalendar events, which are sent by email and can be integrated as WebCal into calendar tools such as Google Calendar.
- New process module: `Live` 💬
  - This allows you to directly reply to customer requests
- New home screen widget: Icon widget
  - Add up to 5 icons linking to experiences.
- Migrated bots and experiences to BPMN XML files
  - Bots and experiences can be exported as XML files, providing overview over the complete configuration of bots and experiences including texts, variables collected etc.
  - All XML files are versioned and backed up internally, giving you the chance for rollbacks if needed. If you need a rollback, please contact our support and we can help you.


### Fixed

- Viber fixes

## release-2020-11-16

### Added

- Add option to request attributes from ProCampaign
- Add restart parameter for widget
- Add option to ask for Opt-Ins again in chat
- Add API servlet to start process flow
- Extended Salesforce integration
  - Allow upserting objects according to fields

## release-2020-11-09

### Added

- New Process module: Language selection
  - This enables you to ask your customer for her/his language.
  - Possible choices are derived from the languages of the BPMN process.
- Locales `de` and `de__formal` can now be active at the same time on the same process, enabling customers to choose between `Duzen` and `Siezen`.


## release-2020-11-02

### Added

- 📧 Process module `Mail`:
  - Sends email in the process flow to the current customer.
- Process module `Signal`.
  - Most process modules emit events. Now you can place a `Signal` process module in any process of the bot, which listens for such events in the bot. When an events occurs, the `Signal` process module is triggered in a background process execution. E.g. a use case is to listen for newsletter opt-in events in any process of the bot and trigger a background process, which writes the newsletter opt-in to Salesforce.
- Added the functions [`string_replace`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replace(java.lang.CharSequence,%20java.lang.CharSequence)) and [`string_replace_all`](https://docs.oracle.com/javase/7/docs/api/java/lang/String.html#replaceAll(java.lang.String,%20java.lang.String)), which can be used in expressions.


## release-2020-10-26

### Added

- `Reminder` process module
  - Schedule reminder notifications for Web push, email etc. individually for your customers, which have given a reminder opt-in.
  - Reminder schedules from menu item "Push" can now be found in the `Reminder` process module, which you can add to any process.
- Refactured campaigns
  - Campaigns now are more lightweight, focussing on Web push: Simply (1) enter a title, body and URL, (2) optionally select you target customer segment, (3) optionally precalculate the segment size and (4) finally trigger sending of Web push notifications to the selected customer segment. Web push notifications will be sent instantly, without planning overhead.
- `Salesforce` process module
  - Integrate Salesforce into experiences in form of a process module with the new `Salesforce` process module. You can map arbitrary customer variables to Salesforce data objects and attributes.
- Background BPMN processes
  - Some integrations can now trigger background BPMN processes. E.g. the Salesforce integration now can be configured with a specific BPMN process, which then can contain the new Salesforce process module.


## release-2020-10-14

### Added

- 🖼️ The carousel component got a rework
  - Video galleries, image galleries, product galleries, prizes, rewards etc. now are presented with a smooth slider
  - The slider teases successive elements of the gallery, giving the chat a horizontal dimension
- 📤 Add a catch-all subscription with whitelist for Pub/Sub
  - Allows all types of events to be sent to a Pub/Sub topic.
  - Event types to pusblish by Pub/Sub can be configured in integration settings.


## release-2020-10-06

### Added

- 💬 Refined Natural Language Processing (NLP) pipeline:
  - NLP models can now be trained by bot (before by tenant).
  - NLP models are stored in a storage after training.
  - NLP training can be canceled.


## release-2020-09-29

### Added

- 📋📋📋 New process module `Decision table` for central evaluation and exection of bpmn process variables and other conditions.
  - If your process tends to be too complicated with many branches this process module might help you in simplifying your process
  - It is an implementation of the open DMN standard by the [OMG group](https://www.omg.org/)
- When a new user message arrives, process information such as bot, experience and process module are now stored additionally.
  - This provides you with information about what a user has entered in which context and can be explored in the live menu.
- 🎞️ Image sharing via new `Image Sharing` process module:
  - Images sent via Snapshot are pre-selected for sharing
- 👶🧒👵 A minimum age can be set for the birthdate
  - In the LoyJoy chat UI only years in accordance with this minimum age can be selected

### Fixed

- 🔗 Links are parsed correctly in questionnaire answers


## release-2020-09-25

### Added

- Intent groups can now be scoped to a bot
  - This enables you to activate specific Intent groups for specific bots.
- ⭐⭐⭐⭐⭐ New process module for creating reviews in Yotpo
  - Including the ability to use the trusted vendors feature
- The coin image is now editable for Loyalty programs
- An image can now be used as a chat background

## release-2020-09-14

### Added

- `Mini program` process module:
  - Allow for multiple variables to be set at the same time
  - Allow blocking process flow until variables are set from within the mini program

## release-2020-09-07

### Added

- Complete switch to NoSQL database repositories for scalability.
- Timers are evaluated on all experiences, not only on default experiences.
- Support for Google Data Studio.
- Extended customer cleansing logic.

## release-2020-08-26

### Added

- The home view is now based on widgets, which can be added flexibly:
  - Widget types to choose from are `hero`, `stories`, `groups`, `notifications`, `roster`. This list will grow in the future.
  - The widget type `stories` enables you to build AMP stories e.g. with https://makestories.io/ and publish them in the home view.
  - As customers can jump from stories into experiences, stories are an exciting way to engage your customers to start chats.
- ✨ Sparkle animation for quiz answer options.
- `Mini program` process module
  - Added action to close Mini-Program via API.
- 🎟️ `Coupon Codes` process module
  - Message, if no coupon codes left.
  - Number of uploaded / redeemed coupon codes in analytics.
  - Allow GS-1 Databar Expanded coupon codes.
- Updated names for sub-processes
  - Show both type and name of a process module together.
- Added copy option for i18n texts to copy texts of an BPMN process from one locale to another.
- Beta REST API for reading and writing customer variables and process variables programmatically.


## release-2020-08-10

### Added

- Extended process variable picker, providing process selection and information about variable declarations.
- Added support for SMS and WhatsApp via Twilio.
- Extended Web service integrations with URLs for process variables, customer variables and session variables. This enables you to listen for any changes to such variables via HTTP POST requests to an API provided by you.

### Changed

- Texts tab revised
  - Search updates only when search text changes.
  - Search also works on placeholder texts.
  - Adjusted layout.
- `Sign in` process module reworked
  - Text before login can now be changed at sign in process module.
  - PIN-E-Mail reworked.
- `Rewards` process module
  - Message if reward is not available
  - Reward redemption counts in analytics
- `Web service` process module
  - Moved HTTP header authorization details to separate field, which can be configured in the Web service process module


## release-2020-07-28

### Added

- Replaced roster view of Web chat with new home view.
  - Content of home view is based on process groups
  - Home view can be themed according to multi-brand / multi-bot Web chat app.
  - Roster is now component in home view.
- 🔔 Push conditions.
  - Push can be made dependent on process & customer variables.
  - Customers can be targeted e.g. by entered data or giveaway participations.
  - Shows number of messages to be sent.
- ↩️ Restart button added to chat menu.

### Changed

- Unified database backend for campaign notifications and reminder notifications, preparing push capabilities for Web chat.

### Fixed

- Customer variables are updated before integration listeners are triggered


## release-2020-07-06

### Added

- Logging is accessible unter settings > log. Unsuccessful integration HTTP calls are logged and can be analyzed there.
- Enhanced Viber integration.
- ProCampaign consumer account assurance.
- New animations.

### Changed

- Switched from birthday to birthdate.

### Fixed

- Fixed CSV export encoding.


## release-2020-06-24

### Added

- Customer referrals.
  - Sharing with customer tokens.
  - Referring customers get loyalty points for new signups.
- Added process groups for structuring processes into roster entries. Refactored the bots management UI around those process groups.
- Added intent groups for structuring intents. Intent groups can be copied between tenants.
- Integration of Viber REST API for Russian market.
- Integration of SMS.
- Barcode scanning for third-party messengers.
- Activated NoSQL database repositories.
- Version indicator in footer of management backend.

### Changed

- Moved coupon codes from experience to process module.

### Fixed

- Multiple choice questions now work on third-party messengers.
- Fix for using LoyJoy inside cross-origin iframes.


## release-2020-06-09

### Added

- Integration mappings can read process variables.
  - Allows sending e.g. customer variables to ProCampaign, Salesforce, Cleverreach etc.
- Historization of customer variables and process variables.
  - When adding a new variable, an existing variable of the same name will be archived
- ⏲️ Timer date change.
  - Previously the timer was listening to a fixed minute interval
  - Now it can be set to be active after a date change (on the next calendar day)
  - Customers can chat at 23:50 and on 00:00 the timer will be active
  - Allows synchronizing daily giveaways & timers
  - Can be used in combination with minute threshold (timer should be active after at least 6 hours & a date change)
- 📅 Date picker for manager preview.
  - Now arbitrary dates can be selected in the manager when working on chat flow.
  - Useful for designing chat flows of time-dependent chat flows such as advent calendars and date-specific giveaways.
- Support for both SQL and NoSQL database repositories.
- Sub processes can be named in a model for better overview.
- CSV export for free-text messages.

### Changed

- Streamlined Web push subscription data model.


## release-2020-05-30

### Added

- 🏆 New `Loyalty` process module enabling loyalty programs.
- Chat can have width in interval XS, SM, MD, LG, XL.
- External links based on i18n entries, enabling language-specific and date-specific links.
- Variable picker and link picker in i18n text entry component.
- Loading indicator and animation for mini programs.
- Mini programs can set process variables via `parent.postMessage({ action: 'setVariable', key: 'somekey', value: 'somevalue' }, '*')`.
- Copy option for questionnaire questions and answer options.
- 🌤️ Integration for weather API.
- New animations.

### Changed

- Palette open by default.
- Bumped dependency versions.

### Fixed

- Fixes on questionnaire chat UI components.
- Fixes for WhatsApp integration.


## release-2020-05-03

### Added

- Persistent chat messages and roster view.
- Unified jump process module.
- Variables in I18n messages and emails.
- `Timer` process module for timed push messages.
- Intro message in proceed process module.
