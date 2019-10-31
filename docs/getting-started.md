 # Getting Started

The Signal Kit API provides school districts with the ability to communicate with their population. Before getting started, here are a few basic guidelines that apply to this collection of API endpoints.

## Authentication

In order to interact with the Signal Kit API, your requests must be authenticated using the OAuth2 workflow. You can get your API key and secret from our support team. These credentials will give an authenticated user access to control the district. Please keep them safe.

Using curl, you can easily test that your keys are working as expected:

```bash
curl -X POST -d "grant_type=client_credentials" -u "<key>:<secret>" https://app.signalkit.com/oauth/token/
```

Sending the request above, you should get a response similar to:

```bash
{"access_token": "6TufJ3HA9IaKDFk1aBlsiCgL6WHry2", "scope": "read delete write", "token_type": "Bearer", "expires_in": 36000}%
```

Once you have this Bearer access_token, you just need to add an Authorization header to your API requests. For example:

```bash
curl -X GET https://app.signalkit.com/api/users/v1/users/ -H 'Authorization: Bearer 6TufJ3HA9IaKDFk1aBlsiCgL6WHry2' 
```

## Request Format

Unless otherwise noted, Signal Kit API endpoints accept and return data using the **application/json** content type.
