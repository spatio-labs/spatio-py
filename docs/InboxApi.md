# spatio.InboxApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_inbox_counts**](InboxApi.md#get_inbox_counts) | **GET** /v1/inbox/counts | Per-bucket unread counts.
[**list_inbox**](InboxApi.md#list_inbox) | **GET** /v1/inbox | Unified inbox feed across mail, channel mentions, DMs, system notifications.
[**mark_inbox_item_read**](InboxApi.md#mark_inbox_item_read) | **PATCH** /v1/inbox/{id}/read | Mark a single inbox item as read.
[**workspace_get_inbox_counts**](InboxApi.md#workspace_get_inbox_counts) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox/counts | 
[**workspace_list_inbox**](InboxApi.md#workspace_list_inbox) | **GET** /v1/organizations/{org}/workspaces/{workspace}/inbox | 
[**workspace_mark_inbox_item_read**](InboxApi.md#workspace_mark_inbox_item_read) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/inbox/{id}/read | 


# **get_inbox_counts**
> InboxCounts get_inbox_counts()

Per-bucket unread counts.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.inbox_counts import InboxCounts
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
    api_instance = spatio.InboxApi(api_client)

    try:
        # Per-bucket unread counts.
        api_response = api_instance.get_inbox_counts()
        print("The response of InboxApi->get_inbox_counts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->get_inbox_counts: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**InboxCounts**](InboxCounts.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Counts. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_inbox**
> InboxListResponse list_inbox(category=category, unread_only=unread_only, limit=limit)

Unified inbox feed across mail, channel mentions, DMs, system notifications.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.inbox_list_response import InboxListResponse
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
    api_instance = spatio.InboxApi(api_client)
    category = 'category_example' # str |  (optional)
    unread_only = True # bool |  (optional)
    limit = 56 # int |  (optional)

    try:
        # Unified inbox feed across mail, channel mentions, DMs, system notifications.
        api_response = api_instance.list_inbox(category=category, unread_only=unread_only, limit=limit)
        print("The response of InboxApi->list_inbox:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->list_inbox: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **category** | **str**|  | [optional] 
 **unread_only** | **bool**|  | [optional] 
 **limit** | **int**|  | [optional] 

### Return type

[**InboxListResponse**](InboxListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Inbox items + counts envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mark_inbox_item_read**
> mark_inbox_item_read(id)

Mark a single inbox item as read.

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
    api_instance = spatio.InboxApi(api_client)
    id = 'id_example' # str | 

    try:
        # Mark a single inbox item as read.
        api_instance.mark_inbox_item_read(id)
    except Exception as e:
        print("Exception when calling InboxApi->mark_inbox_item_read: %s\n" % e)
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
**204** | Marked read. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Item not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_inbox_counts**
> Dict[str, object] workspace_get_inbox_counts(org, workspace)

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
    api_instance = spatio.InboxApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_get_inbox_counts(org, workspace)
        print("The response of InboxApi->workspace_get_inbox_counts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->workspace_get_inbox_counts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 

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
**200** | Counts |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_inbox**
> Dict[str, object] workspace_list_inbox(org, workspace)

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
    api_instance = spatio.InboxApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_inbox(org, workspace)
        print("The response of InboxApi->workspace_list_inbox:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling InboxApi->workspace_list_inbox: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 

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
**200** | Inbox |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_mark_inbox_item_read**
> workspace_mark_inbox_item_read(org, workspace, id)

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
    api_instance = spatio.InboxApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_mark_inbox_item_read(org, workspace, id)
    except Exception as e:
        print("Exception when calling InboxApi->workspace_mark_inbox_item_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**204** | Marked |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

