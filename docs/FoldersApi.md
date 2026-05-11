# spatio.FoldersApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_email_folder**](FoldersApi.md#create_email_folder) | **POST** /v1/folders | Create an email folder.
[**delete_email_folder**](FoldersApi.md#delete_email_folder) | **DELETE** /v1/folders/{id} | Delete an email folder.
[**list_email_folders**](FoldersApi.md#list_email_folders) | **GET** /v1/folders | List the caller&#39;s email folders.
[**list_folder_emails**](FoldersApi.md#list_folder_emails) | **GET** /v1/folders/{id}/emails | List emails inside a folder.
[**move_emails_to_folder**](FoldersApi.md#move_emails_to_folder) | **POST** /v1/folders/{id}/emails | Move emails into a folder.
[**update_email_folder**](FoldersApi.md#update_email_folder) | **PUT** /v1/folders/{id} | Update an email folder.


# **create_email_folder**
> EmailFolder create_email_folder(create_email_folder_request)

Create an email folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_email_folder_request import CreateEmailFolderRequest
from spatio.models.email_folder import EmailFolder
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
    api_instance = spatio.FoldersApi(api_client)
    create_email_folder_request = spatio.CreateEmailFolderRequest() # CreateEmailFolderRequest | 

    try:
        # Create an email folder.
        api_response = api_instance.create_email_folder(create_email_folder_request)
        print("The response of FoldersApi->create_email_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FoldersApi->create_email_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_email_folder_request** | [**CreateEmailFolderRequest**](CreateEmailFolderRequest.md)|  | 

### Return type

[**EmailFolder**](EmailFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_email_folder**
> delete_email_folder(id)

Delete an email folder.

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
    api_instance = spatio.FoldersApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete an email folder.
        api_instance.delete_email_folder(id)
    except Exception as e:
        print("Exception when calling FoldersApi->delete_email_folder: %s\n" % e)
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
**204** | Deleted. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_email_folders**
> EmailFolderListResponse list_email_folders()

List the caller's email folders.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.email_folder_list_response import EmailFolderListResponse
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
    api_instance = spatio.FoldersApi(api_client)

    try:
        # List the caller's email folders.
        api_response = api_instance.list_email_folders()
        print("The response of FoldersApi->list_email_folders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FoldersApi->list_email_folders: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**EmailFolderListResponse**](EmailFolderListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Folder envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_folder_emails**
> Dict[str, object] list_folder_emails(id)

List emails inside a folder.

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
    api_instance = spatio.FoldersApi(api_client)
    id = 'id_example' # str | 

    try:
        # List emails inside a folder.
        api_response = api_instance.list_folder_emails(id)
        print("The response of FoldersApi->list_folder_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FoldersApi->list_folder_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

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
**200** | Email list (open shape — provider-tied). |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **move_emails_to_folder**
> Dict[str, object] move_emails_to_folder(id, move_emails_request)

Move emails into a folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.move_emails_request import MoveEmailsRequest
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
    api_instance = spatio.FoldersApi(api_client)
    id = 'id_example' # str | 
    move_emails_request = spatio.MoveEmailsRequest() # MoveEmailsRequest | 

    try:
        # Move emails into a folder.
        api_response = api_instance.move_emails_to_folder(id, move_emails_request)
        print("The response of FoldersApi->move_emails_to_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FoldersApi->move_emails_to_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **move_emails_request** | [**MoveEmailsRequest**](MoveEmailsRequest.md)|  | 

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
**200** | Result envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email_folder**
> EmailFolder update_email_folder(id, update_email_folder_request)

Update an email folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.email_folder import EmailFolder
from spatio.models.update_email_folder_request import UpdateEmailFolderRequest
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
    api_instance = spatio.FoldersApi(api_client)
    id = 'id_example' # str | 
    update_email_folder_request = spatio.UpdateEmailFolderRequest() # UpdateEmailFolderRequest | 

    try:
        # Update an email folder.
        api_response = api_instance.update_email_folder(id, update_email_folder_request)
        print("The response of FoldersApi->update_email_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FoldersApi->update_email_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_email_folder_request** | [**UpdateEmailFolderRequest**](UpdateEmailFolderRequest.md)|  | 

### Return type

[**EmailFolder**](EmailFolder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

