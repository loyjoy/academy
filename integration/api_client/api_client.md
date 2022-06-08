# API Client
Make use of the API client module whenever you want to send collected data from LoyJoy to your service, pull data from your service to LoyJoy, or you simply want to trigger external services.

<img width="671" alt="Screenshot 2022-06-08 at 09 03 24" src="https://user-images.githubusercontent.com/23342317/172553002-a0da1427-ff7e-4d7d-85f6-1a9e7e82ce8d.png">

## Basic information
### Request
Start by entering necessary information from your service. If you are not sure what information is involved here, check with the appropriate developer. LoyJoy supports three different kinds of Http authorization methods which are send as the `Authorization` header: Basic, Bearer and OAuth2. Moreover, LoyJoy is able to either send the Http request via `GET`, `POST`, or `PUT`. Next, enter the URL of the endpoint of the service in which you can use LoyJoy variables e.g. https://example.de/some_endpoint?param1=${variable1}. Furthermore, you can also enter specific cookies you want to send within the `Cookie` header.

To send a Http body alongside your request, please use either the methods `POST` or `PUT`. Structure your payload according to your scheme defined by your endpoint. Again, if your not sure, please consult the appropriate developer. Note that you can make use of LoyJoy's variables. For example you can send a JSON as follows.

````
{
  firstname: ${firstname},
  lastname: ${lastname},
  variable1: ${variable1}
}
````

Lastly you can setup any custom header necessary for request by adding header key value pairs.

<img width="663" alt="Screenshot 2022-06-08 at 09 07 50" src="https://user-images.githubusercontent.com/23342317/172553763-dac6c800-9466-4870-a0f5-9dcd96a5aea4.png">

### Response
You can process the response in LoyJoy and map a JSON to variables by adding mappings in the module. This allows external information of your service to be used in the chat. To declare variables in LoyJoy use the field `Target variable in LoyJoy`and to extract information from the JSON in the response use the field `Source field in external system`. Consider the following example.

<img width="688" alt="Screenshot 2022-06-08 at 09 23 33" src="https://user-images.githubusercontent.com/23342317/172556601-2846a659-d05c-4a67-934d-f49814e9a3b9.png">

This mapping requires the JSON payload to have the key `personal_consultant`. For example, consider the following response.

````
{
   "personal_consultant": "John Doe",
   "store_address": {
      street: "Main Street 20",
      "city": "Münster",
      "zipcode": "48147"
}
````

You can then use the variable ${consultant} in the chat. 

To extract nested information of a JSON payload, chain the fields with a dot i.e. to extract the city as the variable city use `store_address.city`.

<img width="675" alt="Screenshot 2022-06-08 at 09 33 06" src="https://user-images.githubusercontent.com/23342317/172558623-acfeacf5-e00b-48a8-96a5-da6406a16222.png">
