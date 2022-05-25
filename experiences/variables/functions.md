# Process module conditions
  # Functions
  ##  Where do you find functions?
    ![Condition - function](functionsWhere.png "Condition - function")
  ##  What are functions used for?
    Functions are used for conditional rendering of process modules. Simply stated:
    You can dynamically decide with functions if a process module will be shown in the chat flow.
  ##  How does it work?
    Functions return a value, which you can compare with a fixed value, the value of a variable or with the return value of a different function
    ![Condition - function](functionsWhere.png "Condition - function")
   
    What kind of functions are existing and how are they used?
    
   ### ArrayLength
    If you possibly got multiple inputs (e.g. a multiple choice question in the questionnaire) the values are saved in an array.
    This functions returns now the legth of that array. Simply stated: It returns the number of values stored in the variable.
    You can use this function on any kind of variables and check if they are empty or have a value stored by checking if ArrayLength returns 0.
    
  ### ClientLocale
    This function returns the language setting of the Browser in a String.
    For example:
    English -> "en"
    German  -> "de"
    To check out all possible values, check out a ![documentation of the language codes](https://www.w3schools.com/tags/ref_language_codes.asp).
    
  ### ConverTimestamptMSToDateTime
    You can use this function to convert a timestamp into a Date.
    It started on 1. January 1970, 00:00.
    You need the following arguments:
    argument1: Timestamp - the number of seconds since 1970
    argument2: Pattern - the kind of pattern you want to get e.g. YY-MM-dd ![Check out the official pattern options](https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html)
    argument3: Timezone id - the id of the timezone of the location you are interested in ![All timezones]https://en.wikipedia.org/wiki/List_of_tz_database_time_zones
   
  ### CustomerAgeYears
    This function calculates the age of the customer based on his date of birth, which is stored in the variable birthdate.
    The variable will be filled automatically if you use the birtdate module.
    
  ### date_from_instant
  
  ### Formatted Date today
    Returns the date of today to a format like dd/MM/YY
    
  ### Formatted Date tomorrow
    Returns the date of tomorrow to a format like dd/MM/YY
    
  ### Get Param
    THis function extracts an argument from the url. Argument 1 is the name of the parameter you want to extract.
    In the url it lookes like this:
    .../pathofcurrenturl?variablename=variablevalue
    or
    .../pathofcurrenturl?variablenam1=variablevalue1&variablename2=variablevalue2
    for multiple parameters.
    
  ### HasBpmnProcessVariable
