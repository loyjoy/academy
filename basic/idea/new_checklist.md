# New Project Checklist 

## 1. Legal topics
- [ ] Data Protection Addendum (DPA) / AVV agreed and signed?
- [ ] Addendum to privacy policy / cookie consent necessary?
- [ ] What type of data will be used/stored? For how long in LoyJoy? (Vault or Transit)
- [ ] Terms of participation for the raffle available?

## 2. Website integration

- [ ] Which pages/URLs?
- [ ] Who is responsible for the website integration management on the client side? (Name and contact details -> person should be briefed upfront)
- [ ] Are these pages suitable for integration?
- [ ] Position of chat bubble on website? (left/right/centered)
- [ ] Design of the chat bubble to make it attractive? (image file)
- [ ] Which call-to-action to drive users? (CTA image or preview message)
- [ ] Chatbot opening behaviour (open on Desktop/Mobile once/always)
- [ ] Test-run on website
- [ ] Cookie banner integration necessary: Do we need to wait for cookie consent? Do we set a z-index to keep LoyJoy chatbot behind the cookie banner? (note: LoyJoy is NOT a marketing cookie)

## 3. Messenger & Social Media integration

- [ ] Which messenger channels?
  + Social Media: url/?loyjoy-open=true (opens the chatbot immediately)
  + IG Stories Swipe-Up, Facebook posts, Paid content
- [ ] Who is responsible for the integration?

## 4. Backend integration

- [ ] Is an integration into existing systems required?
- [ ] Which systems? Is the connection technically possible and required?
- [ ] Who provides necessary credentials like API keys?
- [ ] Who is responsible for the existing systems? Who takes care of testing? (Name and contact details -> person should be briefed upfront)

## 4. Email management

- [ ] Can you provide HTML templates for outgoing emails (code email)? 
- [ ] Sender address of outgoing emails? (default is noreply@ljmdn.com; preferably use AWS SES for sending; alternatively SMTP server of customer at own risk regarding availability and speed of delivery)
- [ ] Email address for incoming customer emails? (will not be shown to the consumer)
- [ ] Will a reminder service be offered?
- [ ] If yes, which system will send the reminder emails?
- [ ] Which system will send the reminder DOI mail?
- [ ] Which HTML template will be used for the reminder DOI mail?
- [ ] Can the LoyJoy token be amended to the reminder link? (to login customers automatically)
- [ ] How will opt-outs of the reminder emails be handled?
- [ ] Are there pages for DOI confirmation and reminder opt-out confirmations?

## 5. Content

- [ ] Who designs the chat flow? (Customer, Agency, LoyJoy?)
- [ ] Do we have a multi language environment?
- [ ] Who delivers assets like images and videos, product descriptions, links?
- [ ] Do we need assets in different languages, videos with subtitles?
- [ ] If we use multiple tenants, what will be the differences between the content / chatflow in the tenants?
- [ ] Will there be a Pre- and/or Post-Phase?
- [ ] Pre Registration with Reminder Mail?
- [ ] Where are animations appropriate and wanted? 

## 6. Natural language processing

- [ ] Will you offer customers to send free text messages? Deactivate field if needed.
- [ ] What’s the fallback message and contact email/phone number for customer inquiries?
- [ ] Define the top 20 questions (“intents”) to be answered and provide training data (10 example questions per intent, answer or process to start)

## 7. General

- [ ] Are external partners involved in the project?
- [ ] User & Roles in LoyJoy, who needs which access role?
- [ ] Tenant setup
- [ ] How many Advent calendars are wanted, one in general or an extra advent calendar for premium customers?
- [ ] What will be the volume of users for the Chatbot?
- [ ] Provide a few examples of former Advent calendars (Videos, Slides, Conversations)
