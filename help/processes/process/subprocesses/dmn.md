## Decision Model and Notation (DMN)

Define a decision table based on decision rules to read and write BPMN process variables at once.


**Input** - By clicking on "Input +" you add another input. The input can be a fixed value, a function, or variable. The value this returns is compared to the rules from top to bottom. If one rule applies the output in the same row is generated.

**Output** - By clicking on "Output +" you add another output. The output is stored in a variable/key whose name you can choose yourself.

**Rules** - By clicking on the rule number you can add an annotation, delete it or move the rule up or down. To edit the rule itself you need to click the box and choose an operator and value.

**Rules settings** - You can choose between "First" and "Rule order" by clicking on "F" / "R". Select "first" if the first matching rule should be applied and "rule order" if every rule should be applied. The default is "first".

### Example

![dmn_example_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/dmn_example.png)

In this example, the value of the "app" variable is checked. If it is equal to the string "true", the decision table sets the value "1" in the variable "result". If it is equal to the string "false", the decision table sets the value "2" in the variable "result".

### Further example

In the next example, we consider the result of a questionnaire with three questions. From these we want to generate a process variable with the value green, yellow or red. If at least one question was answered with red, the value should also be red. If all questions were answered with green, the value should become green and in the remaining cases the value should become yellow.

![dmn_colour_example_demo](https://raw.githubusercontent.com/loyjoy/welcome/master/help/processes/process/subprocesses/dmn_colour_example.png)

Since we cannot realize an **OR** in one line, we create three lines for the case that the output value should become red. We see that the condition in empty cells is automatically considered to be fulfilled. Next, we consider the case where the output value should become green. Since the columns of a row are linked with an **AND**, it is sufficient if we check the value for green in each cell. After that, it is important that "first" was selected in the rule's settings. This makes it possible that we can map all remaining combinations to the output value yellow. Again, we use that the condition in empty cells is automatically considered to be fulfilled.

[_See here detailed description_](https://github.com/loyjoy/academy/blob/main/experiences/modules/detailed/decision_table/decision_table.md)
