# Authentication

Blue uses API client credentials for authentication. You can generate your API credentials either from Ripple under "Tools > API Access Tokens", or WavePro under "Settings > API Access Tokens".

Octo uses the same credentials validation as Ripple, so your existing Ripple API client credentials, if any, will also work in Octo. At the moment, Octo doesn't have the UI to create API keys yet, so you can login to [Ripple](https://app.alphaus.cloud/ripple/) using your Octo credentials, and create your API keys under "Tools > API Access Tokens". If you're having trouble accessing Ripple, don't hesitate to [contact](https://www.alphaus.cloud/en/contact) us directly.

Blue API client credentials consist of two values: a client id and a client secret.

Once you have your API client credentials, you can use them to generate access tokens which you can then use to authorize [Blue REST API](https://alphauslabs.github.io/blueapidocs/) calls through the `Authorization: Bearer <token>` HTTP header.

## Generating access tokens

To generate an API access token, you can either call our [access token endpoints](#access-token-endpoints) directly, or use [`bluectl`](https://alphauslabs.github.io/docs/blueapi/bluectl/).

### Calling the endpoint directly

!!! info "Ripple / Octo"
    ``` sh
    $ curl -X POST \
      -F client_id={client-id} \
      -F client_secret={client-secret} \
      -F grant_type=client_credentials \
      -F scope=openid \
      https://login.alphaus.cloud/ripple/access_token
    ```

!!! info "WavePro"
    ``` sh
    $ curl -X POST \
      -F client_id={client-id} \
      -F client_secret={client-secret} \
      -F grant_type=client_credentials \
      -F scope=openid \
      https://login.alphaus.cloud/access_token
    ```

(The only difference is the endpoint.)

### Using `bluectl`

!!! info "Ripple / Octo"
    ``` sh
    $ bluectl token --client-id {client-id} --client-secret {client-secret}
    ```

!!! info "WavePro"
    ``` sh
    $ bluectl token \
      --client-id {client-id} \
      --client-secret {client-secret} \
      --auth-url https://login.alphaus.cloud/access_token
    ```

## Calling Blue API using access tokens

To call an API in Blue using the generated access token, set the `Authorization: Bearer <token>` HTTP header.

!!! info "Ripple / Octo"
    Using `curl` (and `jq`) to generate token:

    ``` sh
    $ ACCESS_TOKEN=$(curl -X POST \
      -F client_id={client-id} \
      -F client_secret={client-secret} \
      -F grant_type=client_credentials \
      -F scope=openid \
      https://login.alphaus.cloud/ripple/access_token | jq -r .access_token)
    ```

    or `bluectl`:

    ``` sh
    $ ACCESS_TOKEN=$(bluectl token --client-id {client-id} --client-secret {client-secret})
    ```

    Then call the API:

    ```sh
    # Sample Ripple API call:
    $ curl -H "Authorization: Bearer $ACCESS_TOKEN" \
      https://api.alphaus.cloud/m/blue/iam/v1/whoami | jq

    # Sample Octo API call:
    $ curl -H "Authorization: Bearer $ACCESS_TOKEN" \
      https://api.alphaus.cloud/m/blue/cover/v1/me | jq
    ```

!!! info "WavePro"
    Using `curl` (and `jq`) to generate token:

    ``` sh
    $ ACCESS_TOKEN=$(curl -X POST \
      -F client_id={client-id} \
      -F client_secret={client-secret} \
      -F grant_type=client_credentials \
      -F scope=openid \
      https://login.alphaus.cloud/access_token | jq -r .access_token)
    ```

    or `bluectl`:

    ``` sh
    $ ACCESS_TOKEN=$(bluectl token \
      --client-id {client-id} \
      --client-secret {client-secret} \
      --auth-url https://login.alphaus.cloud/access_token)
    ```

    Then call the API:

    ```sh
    $ curl -H "Authorization: Bearer $ACCESS_TOKEN" \
      https://api.alphaus.cloud/m/blue/iam/v1/whoami | jq
    ```

## Using environment variables

You can set the environment variables below if you are using [`bluectl`](https://alphauslabs.github.io/docs/blueapi/bluectl/) and/or any of our [supported client libraries](https://alphauslabs.github.io/docs/blueapi/client-sdks/).

!!! info "Ripple / Octo"
    ``` sh
    ALPHAUS_CLIENT_ID={client-id}
    ALPHAUS_CLIENT_SECRET={client-secret}
    ```

!!! info "WavePro"
    ``` sh
    ALPHAUS_CLIENT_ID={wave-client-id}
    ALPHAUS_CLIENT_SECRET={wave-client-secret}
    ALPHAUS_AUTH_URL=https://login.alphaus.cloud/access_token
    ```

To validate your setup, run the following command:
``` sh
$ bluectl whoami
```

If successful, it will output some information about the authenticated user.

!!! warning
    Setting both Ripple/Octo and WavePro client credentials is not supported. If both are set, authentication will default to Ripple/Octo.

If you're using either `bluectl` or any of our supported client libraries, the authentication flow is as follows. First, it will look for the following environment variables:
``` sh
ALPHAUS_CLIENT_ID
ALPHAUS_CLIENT_SECRET
```

The `ALPHAUS_AUTH_URL` environment variable is optional for Ripple/Octo. For WavePro users, this can be set to:
``` sh
ALPHAUS_AUTH_URL=https://login.alphaus.cloud/access_token
```

In most cases, the environment variables above should be sufficient. If those are not set, it will then look for:
``` sh
ALPHAUS_RIPPLE_CLIENT_ID
ALPHAUS_RIPPLE_CLIENT_SECRET
```

If those are not set, it will finally look for:
``` sh
ALPHAUS_WAVE_CLIENT_ID
ALPHAUS_WAVE_CLIENT_SECRET
```

## Accessing BETA environment

If you want to access our NEXT (BETA) environment, you can do:

```sh
$ curl -H "Authorization: Bearer $(bluectl token \
  --client-id $MY_CLIENT_ID_NEXT \
  --client-secret $MY_CLIENT_SECRET_NEXT --beta)" \
  https://apinext.alphaus.cloud/m/blue/iam/v1/whoami | jq
```

## Accessing non-Blue (legacy) APIs

You can also use `bluectl` to provide access tokens to our non-Blue APIs [here](../apiref/authentication.md). For example:
``` sh
$ curl -H "Authorization: Bearer $(bluectl token)" \
  https://api.alphaus.cloud/m/ripple/user | jq
```

## Access token endpoints

The following are the endpoints used to acquire product-specific access tokens. You will then use these tokens in your calls to the API using the `Authorization: Bearer {token}` HTTP header. Ripple access tokens can both be used for Ripple and Octo endpoints; WavePro access tokens are only valid on WavePro endpoints.

!!! quote ""
    Ripple/Octo endpoint:

    ```
    https://login.alphaus.cloud/ripple/access_token
    ```

!!! quote ""
    WavePro endpoint:

    ```
    https://login.alphaus.cloud/access_token
    ```

To obtain an access token, send a POST message to the access token endpoint using the format described below.

**Request**

```
POST {access-token-url} HTTP1.1
Content-Type: multipart/form-data

{body formdata}
```

| **Name** | **Value** |
|---|---|
| `grant_type` | Valid value(s): `password`, `client_credentials` |
| `client_id` | The client id you received from Alphaus or from API. |
| `client_secret` | The client secret you received from Alphaus or from API. |
| `username` | You account username. Required if `grant_type` is set to `password`. |
| `password` | You account password. Required if `grant_type` is set to `password`. |
| `scope` | Valid value(s): `openid` |

**Response**

``` json
{
  "id_token": "eyJ0eXAiOiJKV1Q...",
  "token_type": "Bearer",
  "expires_in": 86400,
  "access_token": "eyJ0eXAiOiJKV1Q...",
  "refresh_token": "def50200..."
}
```

**Example**

``` sh
$ curl -X POST \
  -F client_id={client-id} \
  -F client_secret={client-secret} \
  -F grant_type=client_credentials \
  -F scope=openid \
  https://login.alphaus.cloud/ripple/access_token
```

---
