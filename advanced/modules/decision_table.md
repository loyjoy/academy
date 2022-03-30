# Decision table

Building a product finder, a skin type test, or something similar was never so easy as with the decision table! You do not have to add every condition to each module. 
For this article, you should know how variables work. If you need help with that, read this (LINK) article first.
To use a decision table you need a questionnaire, a decision table, and some outputs. Outputs can be every process brick. Those are what the customer will see as a result. In this example, we will build a test on which hobby suits best for the customer. As a result (outputs) we have swimming, cycling, and jogging.

<p align="center">
  <img src="unnamed.png" alt="Start" title="Start" width="200"/>
</p>
For example, in a product finder, this would be the product gallery with products that suits best your customer.

### Add a questionnaire
First, you add the questions you want to ask. Add at least two questions. For fewer questions, it does not make sense to use a decision table.

<p align="center">
  <img src="answer1.png" alt="Question" title="Question" width="300"/>
  <img src="answer2.png" alt="Question" title="Question" width="300"/>
  <img src="answer3.png" alt="Question" title="Question" width="300"/>
</p>
Then you choose process variables and values for each question and each answer (LINK TO VARIABLES). Pay attention to the correct spelling!

### Working with the decision table
Now you open the decision table. We need to add as many inputs as you have added questions. Therefore click on “Input +”.

<p align="center">
  <img src="input.png" alt="Add an input" title="Add an input" width="400"/>
</p>

Afterward, add an output by clicking on “Output +”. 

<p align="center">
  <img src="output.png" alt="Add an output" title="Add an output" width="400"/>
</p>

Next, click on the first field under “Input” and select “process variable”. Fill in the name of the process variable of your first question. In the other field under input, you do the same with the other process variables. 

<p align="center">
  <img src="rules.png" alt="Add process variables" title="Add process variables" width="400"/>
</p>

Then, click on the field under “Output”, choose again “process variable”, and add a new name. Do not use a name that you have already used. You can use for example “skin type” if you do a skin type test or you can use “product” if you build a product finder. Select 'process specific' for 'Variable scope' if you want the variable to be used only in this experience and 'process independent' if you want the variable to be usable in other experiences as well.

<p align="center">
  <img src="output2.png" alt="Choose outputs" title="Choose outputs" width="400"/>
</p>

As a next step, add a new rule.

<p align="center">
  <img src="addRules.png" alt="Add a new rule" title="Add a new rule" width="400"/>
</p>


With this, you determine the combinations of your questionnaire. For example, you have three outputs: jogging, cycling, and swimming add a rule for every 
combination after which comes jogging as an output. Because of length, we do only three combinations. Afterward, the system will be clear. If the first 
combination is clicked by the customer the hobby will be cycling. So we add in the fields of the first rule values which suits. The system is similar to 
the variables at process bricks. Click on the field under the first input. Choose an operator and add the fitting value. This has to be a value that is 
set in the first question.

<p align="center">
  <img src="rules2.png" alt="Add rules" title="Add rules" width="400"/>
</p>

Then you add the values in the other fields of your inputs too.

<p align="center">
  <img src="rulesReady.png" alt="Complete rules" title="Complete rules" width="400"/>
</p>

Next, you fill in the “Output”. Therefore click on the field under hobby. Choose a fixed value and add a name that is meaningful. In our case, we will use swimming, jogging, and bicycle. 

<p align="center">
  <img src="fixedValueOutput.png" alt="Complete output" title="Complete output" width="400"/>
</p>


Now the first rule is ready. If this combination is clicked, the consumer will get “bicycle” as a result. You need to rule every possibility because else the chatbot does not know what to send. There would be no output then.

<p align="center">
  <img src="ready.png" alt="Add process variables" title="Add process variables" width="400"/>
</p>



### Choose your process bricks
As the last step, you need to condition your modules. Therefore click on the small circle at your process brick. 

<p align="center">
  <img src="conditionModules.png" alt="Condition the modules" title="Condition the modules" width="300"/>
</p>


Then choose “hobby” as a process variable in the first field and your output (swimming, jogging, or cycling) as a fixed value in the third field.

<p align="center">
  <img src="conditionReady.png" alt="Condition is ready" title="Condition is ready" width="300"/>
</p>

That's it! Now your chat is customized to the customer's responses.

<p align="center">
   <img src="end.png" alt="Ready" title="Ready" width="200"/>
</p>
