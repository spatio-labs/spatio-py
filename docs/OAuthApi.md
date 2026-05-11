# spatio.OAuthApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_jwks**](OAuthApi.md#get_jwks) | **GET** /.well-known/jwks.json | JSON Web Key Set for id_token verification (RFC 7517).
[**get_o_auth_discovery**](OAuthApi.md#get_o_auth_discovery) | **GET** /.well-known/oauth-authorization-server | OAuth 2.1 authorization server metadata (RFC 8414).
[**get_open_id_configuration**](OAuthApi.md#get_open_id_configuration) | **GET** /.well-known/openid-configuration | OpenID Connect Discovery 1.0 metadata.
[**get_user_info**](OAuthApi.md#get_user_info) | **GET** /oauth2/userinfo | OIDC UserInfo (OpenID Connect Core 1.0 §5.3).
[**oauth_authorize**](OAuthApi.md#oauth_authorize) | **GET** /oauth2/authorize | OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).
[**oauth_introspect**](OAuthApi.md#oauth_introspect) | **POST** /oauth2/introspect | RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.
[**oauth_revoke**](OAuthApi.md#oauth_revoke) | **POST** /oauth2/revoke | RFC 7009 token revocation. Idempotent.
[**oauth_token**](OAuthApi.md#oauth_token) | **POST** /oauth2/token | Exchange authorization code or refresh token for an access token (+ id_token if &#x60;openid&#x60; scope).
[**post_user_info**](OAuthApi.md#post_user_info) | **POST** /oauth2/userinfo | Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.
[**register_o_auth_client**](OAuthApi.md#register_o_auth_client) | **POST** /oauth2/register | Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).


# **get_jwks**
> JWKS get_jwks()

JSON Web Key Set for id_token verification (RFC 7517).

The set of public keys RPs use to verify Spatio-issued
id_tokens. Cached for 5 minutes at the edge. Always includes
the currently-active signing key plus any retired keys that
may still be in circulation (id_token TTL is 1 hour + slack).


### Example


```python
import spatio
from spatio.models.jwks import JWKS
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)

    try:
        # JSON Web Key Set for id_token verification (RFC 7517).
        api_response = api_instance.get_jwks()
        print("The response of OAuthApi->get_jwks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->get_jwks: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**JWKS**](JWKS.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Key set. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_o_auth_discovery**
> DiscoveryDocument get_o_auth_discovery()

OAuth 2.1 authorization server metadata (RFC 8414).

Returns the canonical metadata for the Spatio OAuth 2.1 + OpenID
Connect server. Third-party RPs use this to auto-discover
endpoint URLs, supported scopes, and signing algorithms.

Identical payload to `/.well-known/openid-configuration` —
either path is acceptable; OIDC clients prefer the
openid-configuration alias.


### Example


```python
import spatio
from spatio.models.discovery_document import DiscoveryDocument
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)

    try:
        # OAuth 2.1 authorization server metadata (RFC 8414).
        api_response = api_instance.get_o_auth_discovery()
        print("The response of OAuthApi->get_o_auth_discovery:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->get_o_auth_discovery: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Metadata document. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_open_id_configuration**
> DiscoveryDocument get_open_id_configuration()

OpenID Connect Discovery 1.0 metadata.

Alias of `/.well-known/oauth-authorization-server`. Provided so
OIDC client libraries (NextAuth, Auth.js, oidc-client-ts,
passport-openidconnect) auto-detect Spatio as an OIDC provider
via their `wellKnown` / `discoveryUrl` config field.


### Example


```python
import spatio
from spatio.models.discovery_document import DiscoveryDocument
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)

    try:
        # OpenID Connect Discovery 1.0 metadata.
        api_response = api_instance.get_open_id_configuration()
        print("The response of OAuthApi->get_open_id_configuration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->get_open_id_configuration: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**DiscoveryDocument**](DiscoveryDocument.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Metadata document. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_user_info**
> UserInfoResponse get_user_info()

OIDC UserInfo (OpenID Connect Core 1.0 §5.3).

Returns user claims gated by the scopes on the presenting
access token. `sub` is always returned; `email`, `name`, etc.
require their respective scopes.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.user_info_response import UserInfoResponse
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (Personal Access Token (pat_...)): bearerAuth
configuration = spatio.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)

    try:
        # OIDC UserInfo (OpenID Connect Core 1.0 §5.3).
        api_response = api_instance.get_user_info()
        print("The response of OAuthApi->get_user_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->get_user_info: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**UserInfoResponse**](UserInfoResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User claims. |  -  |
**401** | Token invalid. |  * WWW-Authenticate -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_authorize**
> oauth_authorize(client_id, redirect_uri, response_type, code_challenge, code_challenge_method, scope=scope, state=state, nonce=nonce, prompt=prompt, max_age=max_age)

OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).

Browser-redirect endpoint. Validates the client + redirect_uri,
packs the request into a signed JWT, and 302s the user's
browser to the consent UI. The consent UI then POSTs to
`/oauth2/authorize/confirm` with the user's decision.

OIDC additions: `scope=openid+profile+email`, `nonce`, `prompt`
(none|login|consent), `max_age`.


### Example


```python
import spatio
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)
    client_id = 'client_id_example' # str | 
    redirect_uri = 'redirect_uri_example' # str | 
    response_type = 'response_type_example' # str | 
    code_challenge = 'code_challenge_example' # str | 
    code_challenge_method = 'code_challenge_method_example' # str | 
    scope = 'scope_example' # str |  (optional)
    state = 'state_example' # str |  (optional)
    nonce = 'nonce_example' # str |  (optional)
    prompt = 'prompt_example' # str |  (optional)
    max_age = 56 # int |  (optional)

    try:
        # OAuth 2.1 authorization endpoint (RFC 6749 + 7636 PKCE).
        api_instance.oauth_authorize(client_id, redirect_uri, response_type, code_challenge, code_challenge_method, scope=scope, state=state, nonce=nonce, prompt=prompt, max_age=max_age)
    except Exception as e:
        print("Exception when calling OAuthApi->oauth_authorize: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**|  | 
 **redirect_uri** | **str**|  | 
 **response_type** | **str**|  | 
 **code_challenge** | **str**|  | 
 **code_challenge_method** | **str**|  | 
 **scope** | **str**|  | [optional] 
 **state** | **str**|  | [optional] 
 **nonce** | **str**|  | [optional] 
 **prompt** | **str**|  | [optional] 
 **max_age** | **int**|  | [optional] 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**302** | Redirect to consent UI or back to redirect_uri with error. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_introspect**
> IntrospectionResponse oauth_introspect(token)

RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.

### Example


```python
import spatio
from spatio.models.introspection_response import IntrospectionResponse
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)
    token = 'token_example' # str | 

    try:
        # RFC 7662 token introspection. Accepts both OAuth access tokens and PATs.
        api_response = api_instance.oauth_introspect(token)
        print("The response of OAuthApi->oauth_introspect:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->oauth_introspect: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**|  | 

### Return type

[**IntrospectionResponse**](IntrospectionResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Introspection result. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_revoke**
> oauth_revoke(token)

RFC 7009 token revocation. Idempotent.

### Example


```python
import spatio
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)
    token = 'token_example' # str | 

    try:
        # RFC 7009 token revocation. Idempotent.
        api_instance.oauth_revoke(token)
    except Exception as e:
        print("Exception when calling OAuthApi->oauth_revoke: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**|  | 

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Revoked (or no-op). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **oauth_token**
> TokenResponse oauth_token(grant_type, code=code, code_verifier=code_verifier, redirect_uri=redirect_uri, refresh_token=refresh_token, client_id=client_id, client_secret=client_secret)

Exchange authorization code or refresh token for an access token (+ id_token if `openid` scope).

### Example


```python
import spatio
from spatio.models.token_response import TokenResponse
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)
    grant_type = 'grant_type_example' # str | 
    code = 'code_example' # str | Required for authorization_code grant. (optional)
    code_verifier = 'code_verifier_example' # str | PKCE verifier — required for authorization_code grant. (optional)
    redirect_uri = 'redirect_uri_example' # str |  (optional)
    refresh_token = 'refresh_token_example' # str | Required for refresh_token grant. (optional)
    client_id = 'client_id_example' # str |  (optional)
    client_secret = 'client_secret_example' # str |  (optional)

    try:
        # Exchange authorization code or refresh token for an access token (+ id_token if `openid` scope).
        api_response = api_instance.oauth_token(grant_type, code=code, code_verifier=code_verifier, redirect_uri=redirect_uri, refresh_token=refresh_token, client_id=client_id, client_secret=client_secret)
        print("The response of OAuthApi->oauth_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->oauth_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **grant_type** | **str**|  | 
 **code** | **str**| Required for authorization_code grant. | [optional] 
 **code_verifier** | **str**| PKCE verifier — required for authorization_code grant. | [optional] 
 **redirect_uri** | **str**|  | [optional] 
 **refresh_token** | **str**| Required for refresh_token grant. | [optional] 
 **client_id** | **str**|  | [optional] 
 **client_secret** | **str**|  | [optional] 

### Return type

[**TokenResponse**](TokenResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/x-www-form-urlencoded
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Token pair (and id_token when applicable). |  -  |
**400** | Invalid grant. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_user_info**
> UserInfoResponse post_user_info()

Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.user_info_response import UserInfoResponse
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (Personal Access Token (pat_...)): bearerAuth
configuration = spatio.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)

    try:
        # Same as GET /oauth2/userinfo. Provided for clients that send the bearer in the body.
        api_response = api_instance.post_user_info()
        print("The response of OAuthApi->post_user_info:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->post_user_info: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**UserInfoResponse**](UserInfoResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User claims. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **register_o_auth_client**
> ClientRegistrationResponse register_o_auth_client(client_registration_request)

Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).

Returns a fresh `client_id` (and, for confidential clients,
`client_secret`) plus a one-time `registration_access_token`
the client can use later to update its registration. Public
clients (mobile, SPA) MUST use `token_endpoint_auth_method:
none` and PKCE.

Rate-limited to 10 registrations per hour per source IP.


### Example


```python
import spatio
from spatio.models.client_registration_request import ClientRegistrationRequest
from spatio.models.client_registration_response import ClientRegistrationResponse
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.OAuthApi(api_client)
    client_registration_request = spatio.ClientRegistrationRequest() # ClientRegistrationRequest | 

    try:
        # Register a new OAuth 2.1 client (RFC 7591 dynamic client registration).
        api_response = api_instance.register_o_auth_client(client_registration_request)
        print("The response of OAuthApi->register_o_auth_client:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OAuthApi->register_o_auth_client: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_registration_request** | [**ClientRegistrationRequest**](ClientRegistrationRequest.md)|  | 

### Return type

[**ClientRegistrationResponse**](ClientRegistrationResponse.md)

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Client registered. |  -  |
**400** | Invalid metadata. |  -  |
**429** | Rate limit exceeded. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

