# spatio.ActionsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**execute_action**](ActionsApi.md#execute_action) | **POST** /v1/actions/execute | Renderer-side execute alias. The canonical endpoint is &#x60;POST /v1/agent/actions/execute&#x60;; this path delegates to the same handler. 
[**get_core_action**](ActionsApi.md#get_core_action) | **GET** /v1/actions/core/{id} | Fetch a single core action by id.
[**list_available_actions**](ActionsApi.md#list_available_actions) | **GET** /v1/actions/available | List every action the agent platform exposes.
[**list_core_actions**](ActionsApi.md#list_core_actions) | **GET** /v1/actions/core | List renderer-curated \&quot;core actions\&quot; (command-palette + keybindings backing).
[**list_core_actions_by_platform**](ActionsApi.md#list_core_actions_by_platform) | **GET** /v1/actions/core/platform/{platform} | Core actions filtered to one platform.
[**list_platform_actions**](ActionsApi.md#list_platform_actions) | **GET** /v1/actions/platform/{platform} | List actions tagged for a specific platform (notes, mail, ...).


# **execute_action**
> ExecuteActionResponse execute_action(execute_action_request)

Renderer-side execute alias. The canonical endpoint is `POST /v1/agent/actions/execute`; this path delegates to the same handler. 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.execute_action_request import ExecuteActionRequest
from spatio.models.execute_action_response import ExecuteActionResponse
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
    api_instance = spatio.ActionsApi(api_client)
    execute_action_request = spatio.ExecuteActionRequest() # ExecuteActionRequest | 

    try:
        # Renderer-side execute alias. The canonical endpoint is `POST /v1/agent/actions/execute`; this path delegates to the same handler. 
        api_response = api_instance.execute_action(execute_action_request)
        print("The response of ActionsApi->execute_action:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->execute_action: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **execute_action_request** | [**ExecuteActionRequest**](ExecuteActionRequest.md)|  | 

### Return type

[**ExecuteActionResponse**](ExecuteActionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Execution result. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_core_action**
> CoreAction get_core_action(id)

Fetch a single core action by id.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.core_action import CoreAction
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
    api_instance = spatio.ActionsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch a single core action by id.
        api_response = api_instance.get_core_action(id)
        print("The response of ActionsApi->get_core_action:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->get_core_action: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**CoreAction**](CoreAction.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Core action. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_available_actions**
> List[ActionDescriptor] list_available_actions()

List every action the agent platform exposes.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.action_descriptor import ActionDescriptor
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
    api_instance = spatio.ActionsApi(api_client)

    try:
        # List every action the agent platform exposes.
        api_response = api_instance.list_available_actions()
        print("The response of ActionsApi->list_available_actions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->list_available_actions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[ActionDescriptor]**](ActionDescriptor.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Action descriptors (bare array). |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_core_actions**
> CoreActionListResponse list_core_actions()

List renderer-curated \"core actions\" (command-palette + keybindings backing).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.core_action_list_response import CoreActionListResponse
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
    api_instance = spatio.ActionsApi(api_client)

    try:
        # List renderer-curated \"core actions\" (command-palette + keybindings backing).
        api_response = api_instance.list_core_actions()
        print("The response of ActionsApi->list_core_actions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->list_core_actions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**CoreActionListResponse**](CoreActionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Core action envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_core_actions_by_platform**
> CoreActionListResponse list_core_actions_by_platform(platform)

Core actions filtered to one platform.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.core_action_list_response import CoreActionListResponse
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
    api_instance = spatio.ActionsApi(api_client)
    platform = 'platform_example' # str | 

    try:
        # Core actions filtered to one platform.
        api_response = api_instance.list_core_actions_by_platform(platform)
        print("The response of ActionsApi->list_core_actions_by_platform:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->list_core_actions_by_platform: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | 

### Return type

[**CoreActionListResponse**](CoreActionListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Core action envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_platform_actions**
> List[ActionDescriptor] list_platform_actions(platform)

List actions tagged for a specific platform (notes, mail, ...).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.action_descriptor import ActionDescriptor
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
    api_instance = spatio.ActionsApi(api_client)
    platform = 'platform_example' # str | 

    try:
        # List actions tagged for a specific platform (notes, mail, ...).
        api_response = api_instance.list_platform_actions(platform)
        print("The response of ActionsApi->list_platform_actions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ActionsApi->list_platform_actions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | 

### Return type

[**List[ActionDescriptor]**](ActionDescriptor.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Action descriptors (bare array). |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

