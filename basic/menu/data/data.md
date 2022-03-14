## Data
+ Local Storage vs Datenbank
+ Winner drawing
...
### Customer

In the customer tab, you can view all customers who have registered via the sign-in module and have been active in the last 180 days. You can see the email address of these customers and when they registered. 

There are two ways to delete data. Either you delete individual customers using the button behind the corresponding customer or you delete all customers at the same time using the button at the top right. Please note that the deletion process is final. The data cannot be restored. If you do not delete the data, it will automatically be deleted after 180 days if the customer has been inactive during that time. If you want to know more about the GDPR regulations, you can request information by clicking the button in the top right corner.

Using the search bar, you can search for customers by their email address. 

You can also download all customer data as a CSV file.

### Runtime log

The runtime log stores events, which have occurred for the tenant in the last 7 days. Typical log entries e.g. are that customers signed up in the chat, or that errors have happened when communicating with remote REST apis such as Salesforce.

For some log entries the log contains so-called trace IDs. Internally, LoyJoy applies OpenTelemetry to generate telemetry data for each process engine execution. When a process module calls a remote REST api (e.g. WebService module, API-Client module), it provides the trace ID as an HTTP header `X-B3-TraceId` to the remote REST api. The remote REST api then can store the trace id in its log file, thereby enabling correlation of LoyJoy log entries with log entries of the remote REST api.
