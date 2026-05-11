# spatio.AccountApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**change_password**](AccountApi.md#change_password) | **POST** /v1/account/security/password | Change or set the account password.
[**consume_agent_task**](AccountApi.md#consume_agent_task) | **POST** /v1/account/usage/consume-agent-task | Atomic check + increment on the agent-task counter (one slot per turn).
[**get_account_plan**](AccountApi.md#get_account_plan) | **GET** /v1/account/plan | The caller&#39;s subscription tier and status.
[**get_account_tier**](AccountApi.md#get_account_tier) | **GET** /v1/account/tier | Capability + quota envelope for the caller&#39;s tier.
[**get_account_usage**](AccountApi.md#get_account_usage) | **GET** /v1/account/usage | Today&#39;s usage counters across notes, sheets, slides, files, tasks, mail, API.
[**get_agent_task_usage**](AccountApi.md#get_agent_task_usage) | **GET** /v1/account/usage/agent-tasks | Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST &#x60;/v1/account/usage/consume-agent-task&#x60; atomically per turn to gate a tool-using turn. 
[**get_sign_in_methods**](AccountApi.md#get_sign_in_methods) | **GET** /v1/account/security/sign-in-methods | List the linked sign-in methods (password + OAuth providers).
[**list_connected_apps**](AccountApi.md#list_connected_apps) | **GET** /v1/account/connected-apps | List the OAuth clients the calling user has granted access to.
[**list_sessions**](AccountApi.md#list_sessions) | **GET** /v1/account/security/sessions | List active sessions for the caller.
[**revoke_connected_app**](AccountApi.md#revoke_connected_app) | **DELETE** /v1/account/connected-apps/{client_id} | Revoke a connected app and all of its active tokens.
[**revoke_other_sessions**](AccountApi.md#revoke_other_sessions) | **POST** /v1/account/security/sessions/revoke-others | Revoke every session except the caller&#39;s current one.
[**revoke_session**](AccountApi.md#revoke_session) | **DELETE** /v1/account/security/sessions/{id} | Revoke a specific session.


# **change_password**
> change_password(change_password_request)

Change or set the account password.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.change_password_request import ChangePasswordRequest
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
    api_instance = spatio.AccountApi(api_client)
    change_password_request = spatio.ChangePasswordRequest() # ChangePasswordRequest | 

    try:
        # Change or set the account password.
        api_instance.change_password(change_password_request)
    except Exception as e:
        print("Exception when calling AccountApi->change_password: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **change_password_request** | [**ChangePasswordRequest**](ChangePasswordRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Password updated. |  -  |
**400** | Invalid body or password too weak. |  -  |
**401** | Caller is not authenticated, or &#x60;currentPassword&#x60; is wrong. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **consume_agent_task**
> ConsumeAgentTaskResponse consume_agent_task()

Atomic check + increment on the agent-task counter (one slot per turn).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.consume_agent_task_response import ConsumeAgentTaskResponse
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # Atomic check + increment on the agent-task counter (one slot per turn).
        api_response = api_instance.consume_agent_task()
        print("The response of AccountApi->consume_agent_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->consume_agent_task: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ConsumeAgentTaskResponse**](ConsumeAgentTaskResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slot consumed. |  -  |
**401** | Caller is not authenticated. |  -  |
**402** | Free trial expired (&#x60;trial_expired&#x60;). |  -  |
**429** | Daily agent-task limit exceeded. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_plan**
> AccountPlan get_account_plan()

The caller's subscription tier and status.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.account_plan import AccountPlan
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # The caller's subscription tier and status.
        api_response = api_instance.get_account_plan()
        print("The response of AccountApi->get_account_plan:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_account_plan: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountPlan**](AccountPlan.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Plan summary. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_tier**
> AccountTierDetails get_account_tier()

Capability + quota envelope for the caller's tier.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.account_tier_details import AccountTierDetails
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # Capability + quota envelope for the caller's tier.
        api_response = api_instance.get_account_tier()
        print("The response of AccountApi->get_account_tier:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_account_tier: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountTierDetails**](AccountTierDetails.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tier details. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_account_usage**
> AccountUsage get_account_usage()

Today's usage counters across notes, sheets, slides, files, tasks, mail, API.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.account_usage import AccountUsage
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # Today's usage counters across notes, sheets, slides, files, tasks, mail, API.
        api_response = api_instance.get_account_usage()
        print("The response of AccountApi->get_account_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_account_usage: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AccountUsage**](AccountUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage snapshot. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_task_usage**
> AgentTaskUsage get_agent_task_usage()

Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST `/v1/account/usage/consume-agent-task` atomically per turn to gate a tool-using turn. 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_task_usage import AgentTaskUsage
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # Free-trial agent-task counter snapshot. Read-only; does NOT consume a slot. Use POST `/v1/account/usage/consume-agent-task` atomically per turn to gate a tool-using turn. 
        api_response = api_instance.get_agent_task_usage()
        print("The response of AccountApi->get_agent_task_usage:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_agent_task_usage: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AgentTaskUsage**](AgentTaskUsage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Counter snapshot. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sign_in_methods**
> SignInMethods get_sign_in_methods()

List the linked sign-in methods (password + OAuth providers).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.sign_in_methods import SignInMethods
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # List the linked sign-in methods (password + OAuth providers).
        api_response = api_instance.get_sign_in_methods()
        print("The response of AccountApi->get_sign_in_methods:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->get_sign_in_methods: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**SignInMethods**](SignInMethods.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Sign-in methods. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_connected_apps**
> ConnectedAppsListResponse list_connected_apps()

List the OAuth clients the calling user has granted access to.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.connected_apps_list_response import ConnectedAppsListResponse
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # List the OAuth clients the calling user has granted access to.
        api_response = api_instance.list_connected_apps()
        print("The response of AccountApi->list_connected_apps:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->list_connected_apps: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ConnectedAppsListResponse**](ConnectedAppsListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Grants. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sessions**
> SessionListResponse list_sessions()

List active sessions for the caller.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.session_list_response import SessionListResponse
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # List active sessions for the caller.
        api_response = api_instance.list_sessions()
        print("The response of AccountApi->list_sessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->list_sessions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**SessionListResponse**](SessionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_connected_app**
> revoke_connected_app(client_id)

Revoke a connected app and all of its active tokens.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
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
    api_instance = spatio.AccountApi(api_client)
    client_id = 'client_id_example' # str | 

    try:
        # Revoke a connected app and all of its active tokens.
        api_instance.revoke_connected_app(client_id)
    except Exception as e:
        print("Exception when calling AccountApi->revoke_connected_app: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **client_id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Revoked. |  -  |
**404** | No active grant for that client. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_other_sessions**
> RevokeOtherSessionsResponse revoke_other_sessions()

Revoke every session except the caller's current one.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.revoke_other_sessions_response import RevokeOtherSessionsResponse
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
    api_instance = spatio.AccountApi(api_client)

    try:
        # Revoke every session except the caller's current one.
        api_response = api_instance.revoke_other_sessions()
        print("The response of AccountApi->revoke_other_sessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AccountApi->revoke_other_sessions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**RevokeOtherSessionsResponse**](RevokeOtherSessionsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Count of sessions revoked. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_session**
> revoke_session(id)

Revoke a specific session.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
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
    api_instance = spatio.AccountApi(api_client)
    id = 'id_example' # str | 

    try:
        # Revoke a specific session.
        api_instance.revoke_session(id)
    except Exception as e:
        print("Exception when calling AccountApi->revoke_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

void (empty response body)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | Session revoked. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Session not found or not owned by caller. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

