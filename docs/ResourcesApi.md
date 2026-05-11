# spatio.ResourcesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_resource_permission_grants**](ResourcesApi.md#list_resource_permission_grants) | **GET** /v1/resources/{platform}/{resourceId}/permissions | List access grants on a resource (per-resource ACL).
[**revoke_resource_permission_grant**](ResourcesApi.md#revoke_resource_permission_grant) | **DELETE** /v1/resources/{platform}/{resourceId}/permissions/{grantId} | Revoke an access grant.
[**set_resource_permission_grant**](ResourcesApi.md#set_resource_permission_grant) | **POST** /v1/resources/{platform}/{resourceId}/permissions | Create or update an access grant.


# **list_resource_permission_grants**
> Dict[str, object] list_resource_permission_grants(platform, resource_id)

List access grants on a resource (per-resource ACL).

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
    api_instance = spatio.ResourcesApi(api_client)
    platform = 'platform_example' # str | 
    resource_id = 'resource_id_example' # str | 

    try:
        # List access grants on a resource (per-resource ACL).
        api_response = api_instance.list_resource_permission_grants(platform, resource_id)
        print("The response of ResourcesApi->list_resource_permission_grants:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->list_resource_permission_grants: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | 
 **resource_id** | **str**|  | 

### Return type

**Dict[str, object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Grant envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **revoke_resource_permission_grant**
> revoke_resource_permission_grant(platform, resource_id, grant_id)

Revoke an access grant.

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
    api_instance = spatio.ResourcesApi(api_client)
    platform = 'platform_example' # str | 
    resource_id = 'resource_id_example' # str | 
    grant_id = 'grant_id_example' # str | 

    try:
        # Revoke an access grant.
        api_instance.revoke_resource_permission_grant(platform, resource_id, grant_id)
    except Exception as e:
        print("Exception when calling ResourcesApi->revoke_resource_permission_grant: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | 
 **resource_id** | **str**|  | 
 **grant_id** | **str**|  | 

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
**204** | Revoked. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_resource_permission_grant**
> Dict[str, object] set_resource_permission_grant(platform, resource_id, request_body)

Create or update an access grant.

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
    api_instance = spatio.ResourcesApi(api_client)
    platform = 'platform_example' # str | 
    resource_id = 'resource_id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Create or update an access grant.
        api_response = api_instance.set_resource_permission_grant(platform, resource_id, request_body)
        print("The response of ResourcesApi->set_resource_permission_grant:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ResourcesApi->set_resource_permission_grant: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **platform** | **str**|  | 
 **resource_id** | **str**|  | 
 **request_body** | [**Dict[str, object]**](object.md)|  | 

### Return type

**Dict[str, object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Created/updated. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

