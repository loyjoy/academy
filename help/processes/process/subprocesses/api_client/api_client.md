## API Client

Send a `GET` or `POST` request to any URL. You can add a custom payload to your post requests and use variables in this payload using the `${variable}` syntax.

If the URL returns a JSON response, you can use mappings to map a JSON field to a LoyJoy variable.

### Authentication

Currently, there are three possible authentication modes available:

- Basic auth
- Bearer auth
- OAuth2 (Password and Client Credentials flows)
