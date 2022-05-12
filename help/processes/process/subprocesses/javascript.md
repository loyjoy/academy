## JavaScript

Define arbitrary JavaScript code to be executed in the user’s browser. Code
should not contain secrets / secret code as it will be sent unencrypted to the
user’s browser.

### Define variables

You can define a function with the name `evalFunction` in your code. This
function should return an array containing objects with the attributes `key`
and `value` to be set as variables.

Example for such a function:

```javascript
function evalFunction() {
  return [{"key": "somekey", "value": "testvalue"}];
}
```

**Note:** this variable will not be set directly with the key `somekey`. The ID
of the process module will be appended to the given key as a safety measure.

So for example the variable define in the example above would have the key
`somekey_e430ec70_3428_4616_a665_a2b4c68d3dec` if the process module’s ID is
`e430ec70-3428-4616-a665-a2b4c68d3dec`. You can copy the ID directly when
configuring the module.
