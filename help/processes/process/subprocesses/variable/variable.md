## Variable


Set one or multiple variables in the process. This is useful to design personalized experiences.

For the variable target you can configure following settings:

- You have to specify a variable name, i.e. under which name the variable value should be stored. Valid variable names should only contain following characters: `a-z A-Z 0-9 _`
- Optionally, you can define, whether the variable should be stored in the Web browser only (`Browser (Cookie)`), or both the Web browser and the Web server (`Server (Database)`). Storing variables on the Web server makes sense, if you eventually want to download them at a certain point in time.  
- Also you can define, whether the variable should be available only in the current process (`process-specific`), or all processes (`process-independent`). Typically, variables should be `process-specific`, except you want to read them from other processes.

For the variable source you can select, whether the variable value should be

- a `fixed value` (i.e. constant), 
- a value from another `process variable`, or 
- a value from calling a `function`. 

Typically, the option `fixed value` is used. The option `process variable` makes sense to copy a variable to a new variable name. The option `function` can be used to call [functions](/experiences/variables/functions.md) for more complicated use cases such as copying a parameter value into a variable or evaluating time-dependent functions.
