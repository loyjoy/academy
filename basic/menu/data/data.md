## Data
+ Local Storage vs Datenbank
+ Winner drawing
...

1. [Customers](#1-customers)
2. [Consents](#2-consents)
3. [Giveaways](#3-giveaways)
4. [Runtime log](#4-runtime-log)

### 1. Customers

In the customer tab, you can view all customers who have registered via the sign-in module and have been active in the last 180 days. You can see the email address of these customers and when they registered. 

There are two ways to delete data. Either you delete individual customers using the button behind the corresponding customer or you delete all customers at the same 
time using the button at the top right. Please note that the deletion process is final. The data cannot be restored. If you do not delete the data, it will 
automatically be deleted after 180 days if the customer has been inactive during that time. If you want to know more about the GDPR regulations, you can request 
information by clicking the button in the top right corner.

Using the search bar, you can search for customers by their email address. 

You can also download all customer data as a CSV file.

### 2. Consents

In the consents tab you can see which customer has given which consent. The data is sorted by time. The time stamp indicates at which point in time the client gave 
this consent.

There are two ways to delete data. Either you delete individual customers using the button behind the corresponding customer or you delete all customers at the same 
time using the button at the top right. Please note that the deletion process is final. The data cannot be restored. If you do not delete the data, it will
automatically be deleted after 180 days if the customer has been inactive during that time.

Using the search bar, you can search for customers by their email address. 

You can also download all customer data as a CSV file.

### 3. Giveaways

In the giveaway tab, you have the possibility to manage your giveaways and to draw winners. First, select which chatbot the giveaway you want to access is in.

#### Manage giveaways
In this section, you will first see all the winners drawn and below that all the participants. 
There is always an email address for each customer. You can also see all the personal data that has been entered via the corresponding modules. This includes, for example, the postal address. 

In the area of the drawn winners, you can draw as many winners as you want via the button 'draw participation'. You can also export the winners as well as all participants with their data as a CSV. To do this, click on the button for the participants or for the drawn winners.
The data will be automatically deleted 60 days after creation.


### 4. Runtime log

The runtime log stores events, which have occurred for the tenant in the last 7 days. Typical log entries e.g. are that customers signed up in the chat, or that errors have happened when communicating with remote REST apis such as Salesforce.

For some log entries the log contains so-called trace IDs. Internally, LoyJoy applies OpenTelemetry to generate telemetry data for each process engine execution. When a process module calls a remote REST api (e.g. WebService module, API-Client module), it provides the trace ID as an HTTP header `X-B3-TraceId` to the remote REST api. The remote REST api then can store the trace id in its log file, thereby enabling correlation of LoyJoy log entries with log entries of the remote REST api.
