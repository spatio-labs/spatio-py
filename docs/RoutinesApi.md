# spatio.RoutinesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**claim_routine_run**](RoutinesApi.md#claim_routine_run) | **POST** /v1/routines/runs/{id}/claim | Worker claims a queued run.
[**complete_routine_run**](RoutinesApi.md#complete_routine_run) | **POST** /v1/routines/runs/{id}/complete | Worker marks a run complete.
[**create_routine**](RoutinesApi.md#create_routine) | **POST** /v1/routines | Create a routine.
[**delete_routine**](RoutinesApi.md#delete_routine) | **DELETE** /v1/routines/{id} | Delete a routine.
[**get_routine**](RoutinesApi.md#get_routine) | **GET** /v1/routines/{id} | Fetch a routine.
[**list_routine_runs**](RoutinesApi.md#list_routine_runs) | **GET** /v1/routines/{id}/runs | List runs for a routine.
[**list_routines**](RoutinesApi.md#list_routines) | **GET** /v1/routines | List routines for the caller&#39;s workspace.
[**run_routine_now**](RoutinesApi.md#run_routine_now) | **POST** /v1/routines/{id}/run-now | Trigger an ad-hoc run.
[**update_routine**](RoutinesApi.md#update_routine) | **PATCH** /v1/routines/{id} | Update a routine.
[**update_routine_run_progress**](RoutinesApi.md#update_routine_run_progress) | **POST** /v1/routines/runs/{id}/progress | Worker reports progress.


# **claim_routine_run**
> RoutineRun claim_routine_run(id)

Worker claims a queued run.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_run import RoutineRun
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 

    try:
        # Worker claims a queued run.
        api_response = api_instance.claim_routine_run(id)
        print("The response of RoutinesApi->claim_routine_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->claim_routine_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Claimed run. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complete_routine_run**
> RoutineRun complete_routine_run(id, routine_run_complete_request)

Worker marks a run complete.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_run import RoutineRun
from spatio.models.routine_run_complete_request import RoutineRunCompleteRequest
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 
    routine_run_complete_request = spatio.RoutineRunCompleteRequest() # RoutineRunCompleteRequest | 

    try:
        # Worker marks a run complete.
        api_response = api_instance.complete_routine_run(id, routine_run_complete_request)
        print("The response of RoutinesApi->complete_routine_run:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->complete_routine_run: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **routine_run_complete_request** | [**RoutineRunCompleteRequest**](RoutineRunCompleteRequest.md)|  | 

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Completed run. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_routine**
> Routine create_routine(create_routine_request)

Create a routine.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_routine_request import CreateRoutineRequest
from spatio.models.routine import Routine
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
    api_instance = spatio.RoutinesApi(api_client)
    create_routine_request = spatio.CreateRoutineRequest() # CreateRoutineRequest | 

    try:
        # Create a routine.
        api_response = api_instance.create_routine(create_routine_request)
        print("The response of RoutinesApi->create_routine:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->create_routine: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_routine_request** | [**CreateRoutineRequest**](CreateRoutineRequest.md)|  | 

### Return type

[**Routine**](Routine.md)

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

# **delete_routine**
> delete_routine(id)

Delete a routine.

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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete a routine.
        api_instance.delete_routine(id)
    except Exception as e:
        print("Exception when calling RoutinesApi->delete_routine: %s\n" % e)
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

# **get_routine**
> Routine get_routine(id)

Fetch a routine.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine import Routine
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch a routine.
        api_response = api_instance.get_routine(id)
        print("The response of RoutinesApi->get_routine:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->get_routine: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**Routine**](Routine.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Routine. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_routine_runs**
> RoutineRunListResponse list_routine_runs(id)

List runs for a routine.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_run_list_response import RoutineRunListResponse
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 

    try:
        # List runs for a routine.
        api_response = api_instance.list_routine_runs(id)
        print("The response of RoutinesApi->list_routine_runs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->list_routine_runs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**RoutineRunListResponse**](RoutineRunListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Run envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_routines**
> RoutineListResponse list_routines(workspace_id=workspace_id, status=status)

List routines for the caller's workspace.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_list_response import RoutineListResponse
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
    api_instance = spatio.RoutinesApi(api_client)
    workspace_id = 'workspace_id_example' # str |  (optional)
    status = 'status_example' # str |  (optional)

    try:
        # List routines for the caller's workspace.
        api_response = api_instance.list_routines(workspace_id=workspace_id, status=status)
        print("The response of RoutinesApi->list_routines:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->list_routines: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 

### Return type

[**RoutineListResponse**](RoutineListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Routine envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **run_routine_now**
> RoutineRun run_routine_now(id)

Trigger an ad-hoc run.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_run import RoutineRun
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 

    try:
        # Trigger an ad-hoc run.
        api_response = api_instance.run_routine_now(id)
        print("The response of RoutinesApi->run_routine_now:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->run_routine_now: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Created run. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_routine**
> Routine update_routine(id, update_routine_request)

Update a routine.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine import Routine
from spatio.models.update_routine_request import UpdateRoutineRequest
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 
    update_routine_request = spatio.UpdateRoutineRequest() # UpdateRoutineRequest | 

    try:
        # Update a routine.
        api_response = api_instance.update_routine(id, update_routine_request)
        print("The response of RoutinesApi->update_routine:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->update_routine: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_routine_request** | [**UpdateRoutineRequest**](UpdateRoutineRequest.md)|  | 

### Return type

[**Routine**](Routine.md)

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

# **update_routine_run_progress**
> RoutineRun update_routine_run_progress(id, routine_run_progress_request)

Worker reports progress.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.routine_run import RoutineRun
from spatio.models.routine_run_progress_request import RoutineRunProgressRequest
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
    api_instance = spatio.RoutinesApi(api_client)
    id = 'id_example' # str | 
    routine_run_progress_request = spatio.RoutineRunProgressRequest() # RoutineRunProgressRequest | 

    try:
        # Worker reports progress.
        api_response = api_instance.update_routine_run_progress(id, routine_run_progress_request)
        print("The response of RoutinesApi->update_routine_run_progress:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RoutinesApi->update_routine_run_progress: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **routine_run_progress_request** | [**RoutineRunProgressRequest**](RoutineRunProgressRequest.md)|  | 

### Return type

[**RoutineRun**](RoutineRun.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated run. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

