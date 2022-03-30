# Data privacy in LoyJoy Cloud Platform

## Data storage and encryption introduction
- This document shall provide an overview of every possibility to store data in LoyJoy. At LoyJoy it is our goal to minimise the data privacy footprint of each experience built on the platform. If you have any questions please contact us via contact@loyjoy.com.
- LoyJoy may use database tables to store data, including personal identifiable information.
- This data storage can be switched off or on based on the LoyJoy tenant usage profile.
- Alternatively, LoyJoy can store data in the local storage of the end customer's device. If this is not sufficient, data from the local storage can be transferred to existing systems via an API. In this way, storage in LoyJoy can usually be avoided altogether.
- We urge our customers to configure LoyJoy according to the principle of data minimisation.
- Data is solely stored in the European Union with AES encryption.
- Every data that might contain personal identifiable information has an automatic expiration. Additionally, data can be manually deleted at any time.

## Overview of personal data storage options

|No  |Name  |Mandatory  |Functionality  |Automatic expiry  |Expiry based on|  Personal data contained  |
| --- | ---- | ------- | -------------- | ---------------- | ------------- | -------------------------- | 
|  1 |   Chat messages |   Required when using the Live Chat module | Allows you to access the list of recent conversations and read conversation messages in the LoyJoy manager in “Live”.| 7 days | Created at  | Chat messages (AES encrypted)  | 
| 2 | Chat messages for Natural Language Understanding (NLU) | No, suggested when using NLU | Stores free-text chat messages with their NLU classification as in Manager > NLU to review AI performance. | 7 days | Created at | Chat messages from free text entries (AES encrypted) | 
| 3 | Messenger Sessions | Required if using Facebook Messenger, WhatsApp, WeChat | Stores chat sessions in case of Facebook, WhatsApp, WeChat, as those channels do not offer a session database comparable to LocalStorage | 7 days | Created at | Customer ID by the external platform, personal data collected in chatbots |
| 4 | Runtime log | Yes | Stores log entries as in Customers > Log <br> E.g. if applicable customer authentication (fail, pass), external API errors (incl. HTTP body in debug mode) | 7 days | Created at | Email address (AES encrypted), IP address, Message (AES encrypted) |
| 5 | Customer database | No | Stores customer data with a flexible data model (based on key value data). Filled automatically and only in case the customer is authenticated, <br> e.g. via process module Sign In. | 180 days | Last interacted at | Email address (AES encrypted), personal data collected in chatbots |
| 6 | Manager log | Yes | Stores log entries as in Manager > Settings > Log <br> E.g. data access by manager users | 180 days | Created at | LoyJoy manager user email addresses (AES encrypted) |
| 7 | Variables | No | Stores all process variables for export purposes as in Manager > Customers > Experience > Download variables | 60 days | Expires at | Variable values, files (AES encrypted) | 
| 8  Marketing Consents | Only when using process modules Newsletter Optin, Reminder Optin, Profiling Optin, WebPush Optin, can be disabled | Stores consents for export purposes. | 180 days | Created at | Email address (AES encrypted), IP address (AES encrypted) |
| 9 | Coupon codes redeemed | Only when using process modules Coupon or Codes, can be disabled | Stores coupon codes to be emitted to customers. A coupon code emitted to a customer is assigned to that customer, so that it cannot be emitted twice. | 180 days | Created at | Email address (AES encrypted) |
| 10 | Loyalty transactions | Only when using process modules Loyalty, LoyaltyReferral, LoyaltySharing, can be disabled | Stores loyalty transactions which in the chat UI are represented as coins. br E.g. a customer can retrieve 10 coins in a loyalty transaction, spend 2 coins in another loyalty transaction for a reward, leaving the customer with 8 coins and a reward redemption. | 180 days | Created at | Email address (AES encrypted) |
| 11 | Loyalty redemptions | Only when using process module Rewards, can be disabled |Stores reward redemptions by customers originating from loyalty transactions | 60 days | Created at | Email address, firstname, last name, postal address, phone (all AES encrypted) |
| 12 | Raffle Participations | Only when using process module Giveaway Participation or Instant Win, can be disabled | Stores raffle participations, from which a participant randomly can be chosen. <br> Might also store a manually picked random list of participants as a copy of the corresponding participation entry | 60 days | Created at | Email address, firstname, last name, postal address, phone (all AES encrypted) |
