# Getting started

The Signal Kit API provides school districts with the ability to communicate with their population. Before getting started, here are a few basic guidelines that apply to this collection of API endpoints.

## Authentication

In order to interact with the Signal Kit API, your requests must be authenticated using the OAuth2 workflow. You can get your API key and secret from our support team. These credentials will give an authenticated user access to control the district. Please keep them safe.

```bash
curl -X POST -d "grant_type=client_credentials" -u "<key>:<secret>" https://app.signalkit.com/oauth/token/
```

## Request Format

Unless otherwise noted, Signal Kit API endpoints accept and return data using the **application/json** content type.