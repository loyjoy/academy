# API Client
Make use of the API client module whenever you want to send collected data from LoyJoy to your service, pull data from your service to LoyJoy, or you simply want to trigger external services.

<img width="665" alt="Screenshot 2022-06-08 at 08 27 32" src="https://user-images.githubusercontent.com/23342317/172546923-0d202a98-d7cd-4298-97c2-02c9f1b7d3d8.png">

## Basic information
Start by entering necessary settings from your service. If you are not sure what information is involved here, check with the appropriate developer. LoyJoy support three different kinds of Http authorization methods which are send as the _Authorization_ header: Basic, Bearer and OAuth2. Moreover, LoyJoy is able to either send the Http request via _GET_, _POST_, or _PUT_. Next, enter the URL of the endpoint of the service in which you can use LoyJoy variables as a unified expression e.g. https://example.de/some_endpoint?param1=${variable1}. You can also enter specific cookies you want to send within the _Cookie_ header.

To send a Http body message alongside your request, please use either the methods _POST_ or _PUT_. Structure you Http body according to your scheme defined by your endpoint. Again, if your not sure, please consult the appropriate developer. Again, make use of LoyJoy's variables as a unified expression. For example you can send a JSON as follows.

````
{
  firstname: ${firstname},
  lastname: ${lastname},
  variable1: ${variable1}
}
````

