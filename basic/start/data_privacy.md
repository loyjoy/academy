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
