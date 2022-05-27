# Process module conditions
  # Functions
  ##  Where do you find functions?
  
    Option 1: At any process module
    <img width="373" alt="Screenshot 2022-05-25 at 10 21 04" src="https://user-images.githubusercontent.com/77499039/170216504-6363c15f-c8ea-4f66-8057-a2ec64bd544a.png">
    <img width="923" alt="Screenshot 2022-05-25 at 10 24 19" src="https://user-images.githubusercontent.com/77499039/170216767-2bbc9458-50af-43c3-a4f3-8a821f511cc8.png">

    Option 2: At questionnaires for conditional visibility of the answers
    <img width="793" alt="Screenshot 2022-05-25 at 10 28 26" src="https://user-images.githubusercontent.com/77499039/170217734-9b3487b8-22c2-49a0-8dab-3fab06e475d4.png">
    
    Option 3: Anywhere you can set variable value manually
    <img width="729" alt="Screenshot 2022-05-25 at 10 30 26" src="https://user-images.githubusercontent.com/77499039/170218138-9aee580d-bbe0-4d6f-98fa-d03c9c8d2926.png">

    
  ##  What are functions used for?
    Functions are used for conditional rendering of process modules. Simply stated:
    You can dynamically decide with functions if a process module will be shown in the chat flow.
  ##  How does it work?
    Functions return a value, which you can compare with a fixed value, 
    the value of a variable or with the return value of a different function
    ![Condition - function](functionsWhere.png "Condition - function")
   
    What kind of functions are existing and how are they used?
    
   ### ArrayLength
    If you possibly got multiple inputs (e.g. a multiple choice question in the questionnaire) the values are saved in an array.
    This functions returns now the length of that array. Simply stated: It returns the number of values stored in the variable.
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
  
  ### Formatted Date today
    Returns the date of today to a format like dd/MM/YY
    
  ### Formatted Date tomorrow
    Returns the date of tomorrow to a format like dd/MM/YY
    
  ### Get Param
    This function extracts an argument from the url. Argument 1 is the name of the parameter you want to extract.
    In the url it lookes like this:
    .../pathofcurrenturl?variablename=variablevalue
    or
    .../pathofcurrenturl?variablenam1=variablevalue1&variablename2=variablevalue2
    for multiple parameters.
    
  ### HasBpmnProcessVariable
    HasBpmnProcessVariable returns 'true' if the variable has a value and 'false' if the variable has no value.
    
  ### HasDeniedAnySignleOptIn
    HasDeniedAnySignleOptIn returns 'true' if the user who is currently signed-in has ever denied any single-opt-in and 'false' if not.
    
  ### I18nTranslate
    This function returns the set translation in the users current language. The function expects the key for the I18nEntry as argument.
    -------Beispiel?
    
  ### Interpolate
    -------Unterschied zu translate und beispiel?
  
  ### IpAdress
    Returns the IP address of the current device.
    
  ### IsAuthenticated
    Returns 'true' if the user is signed in and 'false' if not.
    
  ### IsMobile
    Returns 'true' if the current user uses a mobile device and 'false' if not.
    
  ### IsoLocalDate
    Returns the local date like 'YYYY-MM-dd'.
    
  ### IsoLocalDateTime
    Returns the local date like 'YYYY-MM-ddThh:mm.fffffffff'.
    
  ### LocalDateDayOfMonth
    Returns the local date like 'dd'.
    
  ### LocalDateDayOfWeek
    Returns the local date day of the week as number like 'E' eg. '3'.
    
  ### LocalDateDayOfYear
    Returns the local date like 'DD' (Day of Year).
    
  ### LocalDateYear
    Returns the local date like 'YYYY'.
    
  ### Newsletter double-opt-in
    ------- wofür ist das argument
    
  ### Newsletter double-opt-in URL
    Returns the URL of the double-opt-in. ----------- richtig?
    
  ### Newsletter single-opt-in
    ------- wofür ist das argument
    
  ### Number of participations
    This function calculates the number of participation of the current giveaway.
    
  ### PadZeroes
    'PadZeroes' is used to pad a number or even a string with zeroes. The first argument is the variable
    which value you want to pad with zeroes. The second argument is the amount of digits the value should have afterwards:
    Argument 1: '12'
    Argument 2: '4'
    '12' -> '0012'
    
  ### Postback payload value
    --------letzte payload answer oder was?
    
  ### Profiling double-opt-in
    --------
    
  ### Profiling double-opt-in URL
    --------
  
  ### Profiling single-opt-in
    --------
    
  ### PushLiteral
    'PushLiteral' adds a value (Argument 2) to the variable (Argument 1). The variable has to be in an array form 
    before (e.g. multiple choice question), which does not mean that the variable needs to contain multiple values.
    
  ### PushVariable
    Just like 'PushLiteral' but it adds the value of a variable to the array. Keep in mind that if you do change 
    the value of the variable you added afterwards, it wont change the values inside the array.
    
  ### RandomInt
    This function returns a random integer between the borders (argument 1 and argument 2) including the borders.
    argument 1: '6'
    argument 2: '8'
    -> possible outcomes: '6', '7', '8'
    
  ### Reminder single-opt-in
    -------
    
  ### Sender ID
    ---wer genau ist der sender
    'Sender ID' returns the ID of the current Sender. It is unique per conversation, even if you are signed-in.
    e.g.: 'b0d6950b-06bc-4e6d-88d6-ca7442eb13c9'
    
  ### SignInToken
    Returns a token unique per session even if you are not signed in.
    e.g.: 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJjdXN0b21lciBpc3MiLCJleHAiOjE2NTUxMTMyMDF9.xBq5X0bBhJygojavvp3ng5NWN-nqZioDoLb4laJLhpY'
    
  ### Text message double-opt-in
    ------- values richtig?
    Returns 'true', if the current user has done the double-opt-in in the sms-opt-in module and 'false' if not.
    
  ### Text message single-opt-in
    ------ values richtig?
    Returns 'true', if the current user has done the signle-opt-in in the sms-opt-in module and 'false' if not.
    
  ### StringContains
    Checks if the given variable (argument 1) contains the string (argument 2). It even works with arrays.
    argument 1: 'hello'
    argument 2: 'll'
    -> true
    argument 1: ['value1', 'value2']
    argument 2: 'ue2'
    -> true
    
  ### StringReplace
    Replaces every occurency of the string that should be replaced. And returns that value. 
    It does not have any impact on the input variable(argument 1). It works on arrays as well.
    argument 1: 'helloll'
    argument 2: 'll'
    argument 3: 'bb'
    -> 'hebbobb'
    argument 1: ['helloll', 'hallo']
    argument 2: 'll'
    argument 3: 'bb'
    -> ['hebbobb', 'habbo']
    
  ### StringReplaceAll
    ----Unterschied?
    
  ### User agent
    Returns the properties of the currently used user agent.
    e.g.:
    'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.64 Safari/537.36'
  
  ### Web push double-opt-in
    Returns 'true' if the user allowed the web push in his browser. Else it returns 'false'
  
  ### Web push single-opt-in
    Returns 'true' if the user allowed the web push in the chat. Else it returns 'false'.
