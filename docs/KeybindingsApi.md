# spatio.KeybindingsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_key_binding**](KeybindingsApi.md#delete_key_binding) | **DELETE** /v1/keybindings/{id} | Reset a binding to its platform default.
[**get_default_key_bindings**](KeybindingsApi.md#get_default_key_bindings) | **GET** /v1/keybindings/defaults | Platform default key bindings (no user customizations applied).
[**list_key_bindings**](KeybindingsApi.md#list_key_bindings) | **GET** /v1/keybindings | User&#39;s merged key bindings (defaults + customizations).
[**reset_all_key_bindings**](KeybindingsApi.md#reset_all_key_bindings) | **POST** /v1/keybindings/reset | Reset every customization to its platform default.
[**update_key_binding**](KeybindingsApi.md#update_key_binding) | **PUT** /v1/keybindings/{id} | Create or update a user key-binding customization.
[**validate_key_binding**](KeybindingsApi.md#validate_key_binding) | **POST** /v1/keybindings/validate | Check whether a proposed binding conflicts with existing ones.


# **delete_key_binding**
> delete_key_binding(id)

Reset a binding to its platform default.

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
    api_instance = spatio.KeybindingsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Reset a binding to its platform default.
        api_instance.delete_key_binding(id)
    except Exception as e:
        print("Exception when calling KeybindingsApi->delete_key_binding: %s\n" % e)
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
**204** | Reset. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_default_key_bindings**
> KeyBindingListResponse get_default_key_bindings()

Platform default key bindings (no user customizations applied).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.key_binding_list_response import KeyBindingListResponse
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
    api_instance = spatio.KeybindingsApi(api_client)

    try:
        # Platform default key bindings (no user customizations applied).
        api_response = api_instance.get_default_key_bindings()
        print("The response of KeybindingsApi->get_default_key_bindings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeybindingsApi->get_default_key_bindings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Default bindings envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_key_bindings**
> KeyBindingListResponse list_key_bindings()

User's merged key bindings (defaults + customizations).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.key_binding_list_response import KeyBindingListResponse
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
    api_instance = spatio.KeybindingsApi(api_client)

    try:
        # User's merged key bindings (defaults + customizations).
        api_response = api_instance.list_key_bindings()
        print("The response of KeybindingsApi->list_key_bindings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeybindingsApi->list_key_bindings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**KeyBindingListResponse**](KeyBindingListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bindings envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reset_all_key_bindings**
> reset_all_key_bindings()

Reset every customization to its platform default.

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
    api_instance = spatio.KeybindingsApi(api_client)

    try:
        # Reset every customization to its platform default.
        api_instance.reset_all_key_bindings()
    except Exception as e:
        print("Exception when calling KeybindingsApi->reset_all_key_bindings: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**204** | Reset. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_key_binding**
> KeyBinding update_key_binding(id, update_key_binding_request)

Create or update a user key-binding customization.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.key_binding import KeyBinding
from spatio.models.update_key_binding_request import UpdateKeyBindingRequest
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
    api_instance = spatio.KeybindingsApi(api_client)
    id = 'id_example' # str | 
    update_key_binding_request = spatio.UpdateKeyBindingRequest() # UpdateKeyBindingRequest | 

    try:
        # Create or update a user key-binding customization.
        api_response = api_instance.update_key_binding(id, update_key_binding_request)
        print("The response of KeybindingsApi->update_key_binding:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeybindingsApi->update_key_binding: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_key_binding_request** | [**UpdateKeyBindingRequest**](UpdateKeyBindingRequest.md)|  | 

### Return type

[**KeyBinding**](KeyBinding.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated binding. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_key_binding**
> ValidateKeyBindingResponse validate_key_binding(validate_key_binding_request)

Check whether a proposed binding conflicts with existing ones.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.validate_key_binding_request import ValidateKeyBindingRequest
from spatio.models.validate_key_binding_response import ValidateKeyBindingResponse
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
    api_instance = spatio.KeybindingsApi(api_client)
    validate_key_binding_request = spatio.ValidateKeyBindingRequest() # ValidateKeyBindingRequest | 

    try:
        # Check whether a proposed binding conflicts with existing ones.
        api_response = api_instance.validate_key_binding(validate_key_binding_request)
        print("The response of KeybindingsApi->validate_key_binding:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KeybindingsApi->validate_key_binding: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **validate_key_binding_request** | [**ValidateKeyBindingRequest**](ValidateKeyBindingRequest.md)|  | 

### Return type

[**ValidateKeyBindingResponse**](ValidateKeyBindingResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Validation result. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

