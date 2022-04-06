# Variables

Do you want to specify that modules will be sent only when certain messages will be chosen in a questionnaire? You can do this with variables!
Therefore, you need the module questionnaire or variable. In this article, we will first use the questionnaire. 

### Prepare the questionnaire

Let´s work with the following example: During the chat, the consumer will be asked whether he likes jogging or riding a bicycle. 
A message should then be sent with tips for suitable clothing for the chosen hobby. If you would only drag and drop the modules, 
all of them would be sent. Instead, use variables to only have the right message sent. With variables, you can set what happens if the consumer clicks on one of those hobby messages.

![Result](firstScreenshot.png "Result")


To do so, first, click on the settings icon.

![Settings](settings.png "Settings")
Afterward, choose a process variable. A meaningful name is suitable here. Our example is about hobbies. That is why the name "hobby" is appropriate.

![Choose process variable](processVariable.png "Choose process variable")

Then you click on the settings icons for both answer options too. 

![Set fixed value](answerOptions.png "Set fixed value")

Here we set a fixed value and not a process variable. Because of transparency, we choose “jogging” and “bicycle”. 

![Set fixed value](fixedValue1.png "Set fixed value")
![Set fixed value](fixedValue2.png "Set fixed value")


### Add variables to modules
Those names are freely selectable. Now we have chosen our variables. As a next step, you choose modules that will be sent after the consumer's decision.
The following step works with every module, we are using the module product overview. At each module, there is a small circle in the right corner. 

![Set a condition at the modules](conditionModule.png "Set a condition at the modules")

Click on it. Afterward, choose “add condition” and fill in the three fields. For this, you need to remember the given names in the questionnaire.

<p align="center">
  <img src="addCondition.png" alt="Set a condition at the modules" title="Set a condition at the modules" width="300"/>
</p>
![Set a condition at the modules](addCondition.png "Set a condition at the modules")

For the first field choose “process variable”. Fill in the given name for the question. In our example, it was a “hobby”. 

![Set a condition at the modules](setCondition3.png "Set a condition at the modules")
![Set a condition at the modules](setCondition4.png "Set a condition at the modules")

When setting a variable it is important to pay attention to spelling. The best is, to capitalize or lowercase all initial letters. Also, avoid the space 
behind your variables. As soon as there is a little difference, the chatbot doesn't recognise the variables as equal. So take your time and double-check, because this can save you a lot of time later!
Next, an operator must be chosen. In our case we use “is equal”.

![Choose an operator](operator.png "Choose an operator")

For the last field, you have to select “fixed value”.

![Choose an operator](setFixedValue.png "Choose an operator")

In this field, enter what was previously entered for one of the answer choices. If this module has a message for consumers who have chosen “riding bicycle” you enter in the last field “bicycle” and the other way round. The same thing you do for the second module. 

![Set a condition at the modules](setCondition3.png "Set a condition at the modules")
![Set a condition at the modules](setCondition4.png "Set a condition at the modules")

If you have more than two answer options you can add more modules as well. Besides, it is possible to condition more than one module for 
the same answer. 
For example, you want to give an interview and tips for the best practice to your consumer, and afterward, he can subscribe to a matching newsletter. 
Just drag and drop all those modules in a row and condition them with the same variable.

### Add more conditions

Besides that, one individual module can have more than one condition for when it is played. To do this, you add another condition.

![Add another condition](moreCondition.png "Add another condition")

Here you can choose whether both conditions must be fulfilled (and) or only one of the two (or). 

![Choose the operator](operator1.png "Choose the operator")

For example, if there were another answer option where the jogging tips should also be played, you would choose "or".

![Two conditions](doubleCondition.png "Two conditions")

If we add a second question instead, where the user has to click on a certain answer for the module to be played, “and” would be suitable.
For example, after the consumer has selected "riding a bicycle", he is also asked whether he wants to ride an ergometer or ride in the fresh air. For 
the rider in the fresh air, there is a product recommendation for sunscreen, and for the rider at home, a recommendation for different series to watch 
on the bike. Here, too, any number of conditions can be added. 

As soon as more than one condition is necessary, however, you should consider whether a decision table is easier to handle.
For more information, please read our article.

### Module: Variable

At the beginning of this article, we mentioned that variables can be set with two modules. Now you know how it works with the questionnaire. Next, you learn how to use the module “variable”. It is not that different from the questionnaire. For example, there are different combinations in which the consumer will be asked if he wants to sign up for the newsletter. So that he is not annoyed, we add a variable to save the answer. Therefore you need a variable. 

![Variable module](variableModule.png "Variable module")

In case you have a decision jump that is asking for signing up, there are the options “yes” and “no”. Both will jump to a module “variable” (two different). 

![Variable module](variableInChat.png "Variable module")
![Variable module](setVariableModules.png "Variable module")

The first module is for “yes” and the second one for “no”. We need an automatic jump because else the second module “variable” will be sent too and the chatbot will save both variables. The brick jumps to the newsletter sign up.

![Condition at automatic jump](automaticJump.png "Condition at automatic jump")

 Then you fill in the fields. It is similar to the questionnaire. We need a process variable and a fixed value. Under the first arrow, you fill in a name for the process variable (for example newsletter). Under the second arrow, you choose a fixed value and add a name. It is advisable to use “newsletter” as the process variable and “yes” (or “no” for the other module).

![Set variables](setUpVariable1.png "Set variables")
![Set variables](setUpVariable2.png "Set variables")

Afterwards, condition every newsletter module and question, if the consumer wants to sign up, with the variable you set in when the consumer says “yes”. 

![Set variables](setUpVariable3.png "Set variables")

You can use variables in many different cases. We made up a few examples to show you how it works!
