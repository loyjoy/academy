# Process module conditions
  # Functions
  ##  Where do you find functions?

   ### Option 1: At any process module
   
   ![Function at module](condition_at_module.png "Function at module") 
   ![Condition in module](condition_in_module.png "Condition in module")

   ### Option 2: At questionnaires for conditional visibility of the answers
   ![Condition in answer](condition_in_answer.png "Condition in answer")

   ### Option 3: Anywhere you can set variable value manually
   ![Set variable](set_variable.png "Set variable")


  ##  What are functions used for?
   Most times functions are used for conditional rendering of process modules. Simply stated:
   With functions you can dynamically decide if a process module will be shown in the chat flow.

  ##  How does it work?
   Functions return a value which you can compare with e.g. a fixed value,
   the value of a variable, or with the return value of a different function.
 
![Condition - function](condition_function.png "Condition function")

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
   To check out all possible values, check out a 
   To check ou all possible values, check out a [documentation of the language codes](www.w3schools.com/tags/ref_languages_codes.asp).
  ### ConvertTimestampMSToDateTime
   You can use this function to convert a timestamp into a formatted Date.
   It started on 1. January 1970, 00:00.
   You need the following arguments:
   argument1: Timestamp - the number of seconds since 1970
   argument2: Pattern - the kind of pattern you want to get e.g. YY-MM-dd
   For more informations, [check out the official pattern options](https://docs.oracle.com/javase/7/docs/api/java/text/SimpleDateFormat.html).
   argument3: Timezone id - the id of the timezone of the location you are interested in [all timezones](https://en.wikipedia.org/wiki/List_of_tz_database_time_zones).

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
   HasBpmnProcessVariable returns 'true' if the variable (parameter 1) has a value and 'false' if the variable has no value.

  ### HasDeniedAnySignleOptIn
   HasDeniedAnySignleOptIn returns 'true' if the user who is currently signed-in has ever denied any single-opt-in and 'false' if not.

  ### I18nTranslate
   This function returns the set translation in the users current language. The function expects the key for the I18nEntry as argument.
   The key should look like this:
   welcome_greeting/1f6fb69a-49a8-47c6-ab8e-b6cd290fa196
   This returns the greeting we put in the welcoming module by ourselves.
   The numbers behind the '/' are the subprocesid. You can find it in the url if you click the process module.

  ### Interpolate
   This functions returns the translation for a key aswell, but it allows dynamic values inside the translation.
   welcome_greeting/1f6fb69a-49a8-47c6-ab8e-b6cd290fa196
   This returns the greeting we put in the welcoming module by ourselves.
   The numbers behind the '/' are the subprocesid. You can find it in the url if you click the process module.

  ### IpAdress
   Returns the IP address of the current device.

  ### IsAuthenticated
   Returns 'true' if the user is signed in and 'false' if not. A user can be authenticated via our sign-in module or via an external authentication service.

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
   Returns 'true', if the current user has done the double-opt-in in the newsletter module opt-in and 'false' if not.
   If you have different newsletters with different tags, use the tag as argument in this function.

  ### Newsletter double-opt-in URL
   Returns the link which is used as double-opt-in confirmation.

  ### Newsletter single-opt-in
   Returns 'true', if the current user has done the single-opt-in in the newsletter opt-in module and 'false' if not.
   If you have different newsletters with different tags, use the tag as argument in this function.

  ### Number of participations
   This function calculates the number of the over all participations in any giveaway of the current user.
   To calculate this number there needs to be a giveaway participation module before.


  ### PadZeroes
   'PadZeroes' is used to pad a number or even a string with zeroes. The first argument is the variable
   which value you want to pad with zeroes. The second argument is the amount of digits the value should have afterwards:
   Argument 1: '12'
   Argument 2: '4'
   '12' -> '0012'

  ### Postback payload value
   Returns the id of the selected value by the user. E.g. if the user selects an element in the product gallery module, you can identify its id.

  ### Profiling double-opt-in
   Returns 'true', if the current user has done the double-opt-in in the Profiling opt-in module and 'false' if not.

  ### Profiling double-opt-in URL
   Returns the link which is used as double-opt-in confirmation.

  ### Profiling single-opt-in
   Returns 'true', if the current user has done the single-opt-in in the Profiling opt-in module and 'false' if not.

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
   Returns 'true', if the current user has done the single-opt-in in the Reminder opt-in module and 'false' if not.

  ### Sender ID
   'Sender ID' returns the ID of the current client. It is unique per conversation, even if you are signed-in.
   e.g.: 'b0d6950b-06bc-4e6d-88d6-ca7442eb13c9'

  ### SignInToken
   Returns a token unique per session even if you are not signed in.
   e.g.: 'eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJjdXN0b21lciBpc3MiLCJleHAiOjE2NTUxMTMyMDF9.xBq5X0bBhJygojavvp3ng5NWN-nqZioDoLb4laJLhpY'
   You can use this code e.g. to prepare a link for your user to let him be already signed in if he clicks it.
   'loyjoy_token=eyJ0...'

  ### Text message double-opt-in
   Returns 'true', if the current user has done the double-opt-in in the sms-opt-in module and 'false' if not.

  ### Text message single-opt-in
   Returns 'true', if the current user has done the single-opt-in in the sms-opt-in module and 'false' if not.

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
   StringReplaceAll changes the string in argument 1 by using a regular expression (argument 2).
   It does not have any impact on the input variable(argument 1). It works on arrays as well.
   argument 1: variable -> contains 'this is an example sentence'
   argument 2: '\s+'
   argument 3: '-'
   -> 'this-is-an-example-sentence
   argument 1: ['Welcome to our', 'platform! Thanks for being here.']
   argument 2: '\s+'
   argument 3: '-'
   -> ['Welcome-to-our', 'platform!-Thanks-for-being-here.']

  ### User agent
   Returns the properties of the currently used user agent.
   e.g.:
   'Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/101.0.4951.64 Safari/537.36'

  ### Web push double-opt-in
   Returns 'true' if the user allowed the web push in his browser. Else it returns 'false'

  ### Web push single-opt-in
   Returns 'true' if the user allowed the web push in the chat. Else it returns 'false'.
