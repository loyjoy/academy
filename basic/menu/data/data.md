## Data
+ Local Storage vs Datenbank
+ Winner drawing
...


### Runtime log

The runtime log stores events, which have occurred for the tenant in the last 7 days. Typical log entries e.g. are that customers signed up in the chat, or that errors have happened when communicating with remote REST apis such as Salesforce.

For some log entries the log contains so-called trace IDs. Internally, LoyJoy applies OpenTelemetry to generate telemetry data for each process engine execution. When a process module calls a remote REST api (e.g. WebService module, API-Client module), it provides the trace ID as an HTTP header `X-B3-TraceId` to the remote REST api. The remote REST api then can store the trace id in its log file, thereby enabling correlation of LoyJoy log entries with log entries of the remote REST api.
