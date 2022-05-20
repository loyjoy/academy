#### Process module conditions
  ### Functions
  #  Where do you find functions?
    ![Condition - function](functionsWhere.png "Condition - function")
  #  What are functions used for?
    Functions are used for conditional rendering of process modules. Simply stated:
    You can dynamically decide with functions if a process module will be shown in the chat flow.
  #  How does it work?
    Functions return a value, which you can compare with a fixed value, the value of a variable or with the return value of a different function
    ![Condition - function](functionsWhere.png "Condition - function")
   
    What kind of functions are existing and how are they used?
    
   ## ArrayLength
    If you possibly got multiple inputs (e.g. a multiple choice question in the questionnaire) the values are saved in an array.
    This functions returns now the legth of that array. Simply stated: It returns the number of values stored in the variable.
    You can use this function on any kind of variables and check if they are empty or have a value stored by checking if ArrayLength returns 0.
    
  ## ClientLocale
    This function returns the language setting of the Browser in a String.
    For example:
    English -> "en"
    German  -> "de"
    To check out all possible values, check out a [documentation of the language codes](https://www.w3schools.com/tags/ref_language_codes.asp).
    
    
   
