## Signal

Triggers execution by listening for an incoming signal.

The signal module should always be placed behind the stop module or in a seperate experience. Once triggered, the signal module will execute its subsequent modules. The existing chat-flow will not be altered as only background processing actions such as setting process variables or api calls are performed.

Avoid the usage of tenant wide signals wherever possible, as this is a very expensive action.

### Example

Use Signal when working with DOIs

![animation_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/signal_example.png)
