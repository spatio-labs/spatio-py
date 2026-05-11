# spatio.RecordsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_record**](RecordsApi.md#create_record) | **POST** /v1/records | Create a record.
[**create_record_type**](RecordsApi.md#create_record_type) | **POST** /v1/records/types | Create a record type (org-scoped).
[**delete_record**](RecordsApi.md#delete_record) | **DELETE** /v1/records/{id} | Delete a record.
[**get_record**](RecordsApi.md#get_record) | **GET** /v1/records/{id} | Fetch a record.
[**list_record_types**](RecordsApi.md#list_record_types) | **GET** /v1/records/types | List record types for an organization.
[**list_records**](RecordsApi.md#list_records) | **GET** /v1/records | List records for an organization. &#x60;organization_id&#x60; query param is required (handler returns 400 otherwise). 
[**update_record**](RecordsApi.md#update_record) | **PATCH** /v1/records/{id} | Update a record.
[**update_record_type**](RecordsApi.md#update_record_type) | **PATCH** /v1/records/types/{id} | Update a record type.


# **create_record**
> Record create_record(create_record_request)

Create a record.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_record_request import CreateRecordRequest
from spatio.models.record import Record
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
    api_instance = spatio.RecordsApi(api_client)
    create_record_request = spatio.CreateRecordRequest() # CreateRecordRequest | 

    try:
        # Create a record.
        api_response = api_instance.create_record(create_record_request)
        print("The response of RecordsApi->create_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->create_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_record_request** | [**CreateRecordRequest**](CreateRecordRequest.md)|  | 

### Return type

[**Record**](Record.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created record. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_record_type**
> RecordType create_record_type(create_record_type_request)

Create a record type (org-scoped).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_record_type_request import CreateRecordTypeRequest
from spatio.models.record_type import RecordType
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
    api_instance = spatio.RecordsApi(api_client)
    create_record_type_request = spatio.CreateRecordTypeRequest() # CreateRecordTypeRequest | 

    try:
        # Create a record type (org-scoped).
        api_response = api_instance.create_record_type(create_record_type_request)
        print("The response of RecordsApi->create_record_type:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->create_record_type: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_record_type_request** | [**CreateRecordTypeRequest**](CreateRecordTypeRequest.md)|  | 

### Return type

[**RecordType**](RecordType.md)

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

# **delete_record**
> delete_record(id)

Delete a record.

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
    api_instance = spatio.RecordsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete a record.
        api_instance.delete_record(id)
    except Exception as e:
        print("Exception when calling RecordsApi->delete_record: %s\n" % e)
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

# **get_record**
> Record get_record(id)

Fetch a record.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.record import Record
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
    api_instance = spatio.RecordsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch a record.
        api_response = api_instance.get_record(id)
        print("The response of RecordsApi->get_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->get_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**Record**](Record.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_record_types**
> RecordTypeListResponse list_record_types(organization_id)

List record types for an organization.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.record_type_list_response import RecordTypeListResponse
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
    api_instance = spatio.RecordsApi(api_client)
    organization_id = 'organization_id_example' # str | 

    try:
        # List record types for an organization.
        api_response = api_instance.list_record_types(organization_id)
        print("The response of RecordsApi->list_record_types:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->list_record_types: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **str**|  | 

### Return type

[**RecordTypeListResponse**](RecordTypeListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record-type envelope. |  -  |
**400** | Missing organization_id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_records**
> RecordListResponse list_records(organization_id, record_type_id=record_type_id, limit=limit)

List records for an organization. `organization_id` query param is required (handler returns 400 otherwise). 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.record_list_response import RecordListResponse
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
    api_instance = spatio.RecordsApi(api_client)
    organization_id = 'organization_id_example' # str | 
    record_type_id = 'record_type_id_example' # str |  (optional)
    limit = 56 # int |  (optional)

    try:
        # List records for an organization. `organization_id` query param is required (handler returns 400 otherwise). 
        api_response = api_instance.list_records(organization_id, record_type_id=record_type_id, limit=limit)
        print("The response of RecordsApi->list_records:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->list_records: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization_id** | **str**|  | 
 **record_type_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] 

### Return type

[**RecordListResponse**](RecordListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Record envelope. |  -  |
**400** | Missing organization_id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_record**
> Record update_record(id, update_record_request)

Update a record.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.record import Record
from spatio.models.update_record_request import UpdateRecordRequest
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
    api_instance = spatio.RecordsApi(api_client)
    id = 'id_example' # str | 
    update_record_request = spatio.UpdateRecordRequest() # UpdateRecordRequest | 

    try:
        # Update a record.
        api_response = api_instance.update_record(id, update_record_request)
        print("The response of RecordsApi->update_record:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->update_record: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_record_request** | [**UpdateRecordRequest**](UpdateRecordRequest.md)|  | 

### Return type

[**Record**](Record.md)

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

# **update_record_type**
> RecordType update_record_type(id, update_record_type_request)

Update a record type.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.record_type import RecordType
from spatio.models.update_record_type_request import UpdateRecordTypeRequest
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
    api_instance = spatio.RecordsApi(api_client)
    id = 'id_example' # str | 
    update_record_type_request = spatio.UpdateRecordTypeRequest() # UpdateRecordTypeRequest | 

    try:
        # Update a record type.
        api_response = api_instance.update_record_type(id, update_record_type_request)
        print("The response of RecordsApi->update_record_type:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecordsApi->update_record_type: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_record_type_request** | [**UpdateRecordTypeRequest**](UpdateRecordTypeRequest.md)|  | 

### Return type

[**RecordType**](RecordType.md)

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

