
1. [Customers](#1-customers)
2. [Consents](#2-consents)
3. [Giveaways](#3-giveaways)
4. [Instant win](#4-instant-win)
5. [Runtime log](#5-runtime-log)

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

In the area of the drawn participations, you can draw as many winners as you want via the button 'draw participation'. You can also export the winners as 
well as all participants with their data as a CSV. To do this, click on the button for the participants or for the drawn winners.
The data will be automatically deleted 60 days after creation.

#### Participations
In this area, you can see all participants. You can also see all the data that the participant has entered. If, for example, you were asked for the 
postal address in the chat, it will be displayed here. You can also see in which experience the customer took part in the competition and when.
You can either delete the data individually via the bin symbol or you can delete all of them via the button 'Delete all entries' at the top right. If you 
do not delete the data yourself, it will be deleted automatically after 60 days.

#### Drawn participations
Here you can see all the participants drawn. You can see all the personal information that was asked for in the chatbot, such as the postal address. In 
addition, under 'created at' you can see when the participant was drawn and under 'participated at' when the customer participated.You can either delete 
the data individually via the bin symbol or you can delete all of them via the button 'Delete all entries' at the top right. If you 
do not delete the data yourself, it will be deleted automatically after 60 days.

### 4. Instant win
This area is structured in the same way as the tab for [giveaways](#3-giveaways). The only difference is that there is no button for the winner drawing, as these have 
already been selected automatically.

### 5. Codes

#### Manage coupons
First, select the experience in which you want to manage the coupons.
You can add new coupons. To do this, either download the example CSV file using the button 'Download example CSV' and then upload it again using the button 
'Upload CSV' or upload your CSV file using this button. CSV files can also be uploaded in the module itself.
You can also see which coupons have already been awarded. You will receive the email of the coupon winner, when they received the coupon (issued at) and 
when the coupon was created.
You have the chance to download the information as a CSV file. The coupon codes are then listed in the file. In addition, the winner and when he or she won 
the coupon is listed.
You can either delete the data individually via the bin symbol or you can delete all of them via the button 'Delete all entries' at the top right. If you 
do not delete the data yourself, it will be deleted automatically after 720 days.

#### Manage codes

#### Coupons
In this section you can see all the coupon codes from the entire tenant. For each code, you can see who won it and when. In addition, you can see in which 
experience it is awarded and when the coupon was added there.
You can either delete the data individually via the bin symbol or you can delete all of them via the button 'Delete all entries' at the top right. If you 
do not delete the data yourself, it will be deleted automatically after 720 days.

### 5. Runtime log

The runtime log stores events, which have occurred for the tenant in the last 7 days. Typical log entries e.g. are that customers signed up in the chat, or that errors have happened when communicating with remote REST apis such as Salesforce.

For some log entries the log contains so-called trace IDs. Internally, LoyJoy applies OpenTelemetry to generate telemetry data for each process engine execution. When a process module calls a remote REST api (e.g. WebService module, API-Client module), it provides the trace ID as an HTTP header `X-B3-TraceId` to the remote REST api. The remote REST api then can store the trace id in its log file, thereby enabling correlation of LoyJoy log entries with log entries of the remote REST api.
