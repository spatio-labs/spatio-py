# spatio.TasksApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_delete_tasks**](TasksApi.md#bulk_delete_tasks) | **POST** /v1/tasks/delete | Delete multiple tasks in one call.
[**bulk_update_tasks**](TasksApi.md#bulk_update_tasks) | **POST** /v1/tasks/bulk-update | Apply the same update to multiple tasks.
[**complete_task**](TasksApi.md#complete_task) | **POST** /v1/tasks/{id}/complete | Mark a task complete.
[**create_task**](TasksApi.md#create_task) | **POST** /v1/tasks | Create a task.
[**create_task_comment**](TasksApi.md#create_task_comment) | **POST** /v1/tasks/{id}/comments | Create a comment.
[**delete_task**](TasksApi.md#delete_task) | **DELETE** /v1/tasks/{id} | Delete a task.
[**delete_task_comment**](TasksApi.md#delete_task_comment) | **DELETE** /v1/tasks/{id}/comments/{commentId} | Delete a task comment.
[**get_task**](TasksApi.md#get_task) | **GET** /v1/tasks/{id} | Fetch one task.
[**list_task_comments**](TasksApi.md#list_task_comments) | **GET** /v1/tasks/{id}/comments | List comments on a task.
[**list_task_providers**](TasksApi.md#list_task_providers) | **GET** /v1/tasks/providers | List supported task providers.
[**list_tasks**](TasksApi.md#list_tasks) | **GET** /v1/tasks | List tasks across connected accounts.
[**update_task**](TasksApi.md#update_task) | **PATCH** /v1/tasks/{id} | Update a task (partial).
[**update_task_comment**](TasksApi.md#update_task_comment) | **PATCH** /v1/tasks/{id}/comments/{commentId} | Edit a task comment.
[**workspace_complete_task**](TasksApi.md#workspace_complete_task) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id}/complete | 
[**workspace_complete_task_alias**](TasksApi.md#workspace_complete_task_alias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/complete/task | Renderer-compat alias for /tasks/{id}/complete.
[**workspace_create_task**](TasksApi.md#workspace_create_task) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks | 
[**workspace_create_task_alias**](TasksApi.md#workspace_create_task_alias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/tasks/task | Renderer-compat alias for POST /tasks.
[**workspace_delete_task**](TasksApi.md#workspace_delete_task) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} | 
[**workspace_get_task**](TasksApi.md#workspace_get_task) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} | 
[**workspace_list_task_providers**](TasksApi.md#workspace_list_task_providers) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/providers | 
[**workspace_list_tasks**](TasksApi.md#workspace_list_tasks) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks | 
[**workspace_list_tasks_alias**](TasksApi.md#workspace_list_tasks_alias) | **GET** /v1/organizations/{org}/workspaces/{workspace}/tasks/tasks | Renderer-compat alias for /tasks.
[**workspace_update_task**](TasksApi.md#workspace_update_task) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/tasks/{id} | 
[**workspace_update_task_alias**](TasksApi.md#workspace_update_task_alias) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/tasks/task/{id} | Renderer-compat alias for PATCH /tasks/{id}.


# **bulk_delete_tasks**
> BulkDeleteTasksResponse bulk_delete_tasks(bulk_delete_tasks_request)

Delete multiple tasks in one call.

Replaces the legacy BFF that looped DELETE /v1/tasks/:id.
Per-id errors are collected in `failed` rather than failing
the whole call — partial success is the norm.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_delete_tasks_request import BulkDeleteTasksRequest
from spatio.models.bulk_delete_tasks_response import BulkDeleteTasksResponse
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
    api_instance = spatio.TasksApi(api_client)
    bulk_delete_tasks_request = spatio.BulkDeleteTasksRequest() # BulkDeleteTasksRequest | 

    try:
        # Delete multiple tasks in one call.
        api_response = api_instance.bulk_delete_tasks(bulk_delete_tasks_request)
        print("The response of TasksApi->bulk_delete_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->bulk_delete_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_delete_tasks_request** | [**BulkDeleteTasksRequest**](BulkDeleteTasksRequest.md)|  | 

### Return type

[**BulkDeleteTasksResponse**](BulkDeleteTasksResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Partial-success envelope. |  -  |
**400** | Body missing or &#x60;taskIds&#x60; empty. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulk_update_tasks**
> BulkUpdateTasksResponse bulk_update_tasks(bulk_update_tasks_request)

Apply the same update to multiple tasks.

Same `updates` payload applied to every id in `taskIds`. As
with bulk delete, per-id failures collect in `failed`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_update_tasks_request import BulkUpdateTasksRequest
from spatio.models.bulk_update_tasks_response import BulkUpdateTasksResponse
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
    api_instance = spatio.TasksApi(api_client)
    bulk_update_tasks_request = spatio.BulkUpdateTasksRequest() # BulkUpdateTasksRequest | 

    try:
        # Apply the same update to multiple tasks.
        api_response = api_instance.bulk_update_tasks(bulk_update_tasks_request)
        print("The response of TasksApi->bulk_update_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->bulk_update_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_update_tasks_request** | [**BulkUpdateTasksRequest**](BulkUpdateTasksRequest.md)|  | 

### Return type

[**BulkUpdateTasksResponse**](BulkUpdateTasksResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Partial-success envelope. |  -  |
**400** | Body missing or &#x60;taskIds&#x60; empty. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **complete_task**
> SuccessFlag complete_task(id, account_id=account_id, x_workspace_id=x_workspace_id)

Mark a task complete.

Idempotent — completing an already-completed task is a no-op
that still returns success. The legacy
`POST /v1/tasks/complete/task` endpoint accepts the same
operation with the task id in the JSON body instead of the
URL; that variant is a renderer-compat shim and is not
modeled in the spec.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.success_flag import SuccessFlag
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Mark a task complete.
        api_response = api_instance.complete_task(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->complete_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->complete_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Task not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_task**
> Task create_task(create_task_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)

Create a task.

Creates a new task under the target account. Target resolution
mirrors `POST /v1/notes`: body `accountId` → `?accountId=` →
body `provider` → `?provider=` → caller's single connected
account (errors `ambiguous_account` if more than one and no
selector).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_task_request import CreateTaskRequest
from spatio.models.task import Task
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
    api_instance = spatio.TasksApi(api_client)
    create_task_request = spatio.CreateTaskRequest() # CreateTaskRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a task.
        api_response = api_instance.create_task(create_task_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->create_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->create_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_task_request** | [**CreateTaskRequest**](CreateTaskRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Task**](Task.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Task created. |  -  |
**400** | Invalid body, ambiguous account (&#x60;code: ambiguous_account&#x60;), or no tasks provider connected (&#x60;code: no_task_provider&#x60;).  |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_task_comment**
> TaskCommentMutationResponse create_task_comment(id, task_comment_request, account_id=account_id, x_workspace_id=x_workspace_id)

Create a comment.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task_comment_mutation_response import TaskCommentMutationResponse
from spatio.models.task_comment_request import TaskCommentRequest
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    task_comment_request = spatio.TaskCommentRequest() # TaskCommentRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a comment.
        api_response = api_instance.create_task_comment(id, task_comment_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->create_task_comment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->create_task_comment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **task_comment_request** | [**TaskCommentRequest**](TaskCommentRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**TaskCommentMutationResponse**](TaskCommentMutationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comment created. |  -  |
**400** | Missing content or task id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_task**
> SuccessFlag delete_task(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a task.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.success_flag import SuccessFlag
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a task.
        api_response = api_instance.delete_task(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->delete_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->delete_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Task not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_task_comment**
> SuccessFlag delete_task_comment(id, comment_id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a task comment.

Allowed for the comment author and (for native comments) for
the task owner.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.success_flag import SuccessFlag
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    comment_id = 'comment_id_example' # str | Comment id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a task comment.
        api_response = api_instance.delete_task_comment(id, comment_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->delete_task_comment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->delete_task_comment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **comment_id** | **str**| Comment id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**400** | Missing comment id. |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is neither the author nor the task owner. |  -  |
**404** | Comment not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task**
> Task get_task(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one task.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task import Task
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one task.
        api_response = api_instance.get_task(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->get_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->get_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Task**](Task.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The task. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Task not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_task_comments**
> TaskCommentList list_task_comments(id, account_id=account_id, x_workspace_id=x_workspace_id)

List comments on a task.

Returns active comments. When `?accountId=` targets an external
provider that supports comments (e.g. Linear), the provider is
queried directly; otherwise the native `TaskComment` table is
used.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task_comment_list import TaskCommentList
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # List comments on a task.
        api_response = api_instance.list_task_comments(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->list_task_comments:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->list_task_comments: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**TaskCommentList**](TaskCommentList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comment list. |  -  |
**400** | Missing task id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_task_providers**
> TaskProvidersInfo list_task_providers()

List supported task providers.

Returns the registered task-provider ids and the platform's
own metadata. Useful for clients that need to render
provider-specific UI (icons, capability flags) before
committing to a particular `provider`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task_providers_info import TaskProvidersInfo
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
    api_instance = spatio.TasksApi(api_client)

    try:
        # List supported task providers.
        api_response = api_instance.list_task_providers()
        print("The response of TasksApi->list_task_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->list_task_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**TaskProvidersInfo**](TaskProvidersInfo.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Provider info. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tasks**
> TaskListEnvelope list_tasks(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, completed=completed, labels=labels, parent_task_id=parent_task_id, type=type, source_platform=source_platform, source_id=source_id, limit=limit, offset=offset)

List tasks across connected accounts.

Fan-out list. Returns every task visible to the caller across
every connected tasks provider. Pass `?accountId=` or
`?provider=` to scope to a single source.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task_list_envelope import TaskListEnvelope
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
    api_instance = spatio.TasksApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    completed = False # bool | Include completed tasks. Default `false` (active tasks only).  (optional) (default to False)
    labels = ['labels_example'] # List[str] | Repeatable. Filter to tasks carrying every label listed. (optional)
    parent_task_id = 'parent_task_id_example' # str | Filter to subtasks of this parent. (optional)
    type = 'type_example' # str | Discriminator filter (`todo`, `reminder`, `issue`).  (optional)
    source_platform = 'source_platform_example' # str | Filter to tasks linked to a given source platform. (optional)
    source_id = 'source_id_example' # str | Filter to tasks linked to a specific source artifact id. Pair with `sourcePlatform` for an exact match.  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List tasks across connected accounts.
        api_response = api_instance.list_tasks(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, completed=completed, labels=labels, parent_task_id=parent_task_id, type=type, source_platform=source_platform, source_id=source_id, limit=limit, offset=offset)
        print("The response of TasksApi->list_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->list_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **completed** | **bool**| Include completed tasks. Default &#x60;false&#x60; (active tasks only).  | [optional] [default to False]
 **labels** | [**List[str]**](str.md)| Repeatable. Filter to tasks carrying every label listed. | [optional] 
 **parent_task_id** | **str**| Filter to subtasks of this parent. | [optional] 
 **type** | **str**| Discriminator filter (&#x60;todo&#x60;, &#x60;reminder&#x60;, &#x60;issue&#x60;).  | [optional] 
 **source_platform** | **str**| Filter to tasks linked to a given source platform. | [optional] 
 **source_id** | **str**| Filter to tasks linked to a specific source artifact id. Pair with &#x60;sourcePlatform&#x60; for an exact match.  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**TaskListEnvelope**](TaskListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Fan-out envelope. |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Resolver or fan-out failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_task**
> Task update_task(id, update_task_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a task (partial).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task import Task
from spatio.models.update_task_request import UpdateTaskRequest
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    update_task_request = spatio.UpdateTaskRequest() # UpdateTaskRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a task (partial).
        api_response = api_instance.update_task(id, update_task_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->update_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->update_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **update_task_request** | [**UpdateTaskRequest**](UpdateTaskRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Task**](Task.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated task. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Task not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_task_comment**
> TaskCommentMutationResponse update_task_comment(id, comment_id, task_comment_request, account_id=account_id, x_workspace_id=x_workspace_id)

Edit a task comment.

Only the comment author can edit.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.task_comment_mutation_response import TaskCommentMutationResponse
from spatio.models.task_comment_request import TaskCommentRequest
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
    api_instance = spatio.TasksApi(api_client)
    id = 'id_example' # str | Task id.
    comment_id = 'comment_id_example' # str | Comment id.
    task_comment_request = spatio.TaskCommentRequest() # TaskCommentRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Edit a task comment.
        api_response = api_instance.update_task_comment(id, comment_id, task_comment_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of TasksApi->update_task_comment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->update_task_comment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Task id. | 
 **comment_id** | **str**| Comment id. | 
 **task_comment_request** | [**TaskCommentRequest**](TaskCommentRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**TaskCommentMutationResponse**](TaskCommentMutationResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Comment updated. |  -  |
**400** | Missing content or comment id. |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is not the comment author. |  -  |
**404** | Comment not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_complete_task**
> Dict[str, object] workspace_complete_task(org, workspace, id)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_complete_task(org, workspace, id)
        print("The response of TasksApi->workspace_complete_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_complete_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**200** | Completed |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_complete_task_alias**
> Dict[str, object] workspace_complete_task_alias(org, workspace, request_body)

Renderer-compat alias for /tasks/{id}/complete.

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Renderer-compat alias for /tasks/{id}/complete.
        api_response = api_instance.workspace_complete_task_alias(org, workspace, request_body)
        print("The response of TasksApi->workspace_complete_task_alias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_complete_task_alias: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**200** | Completed |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_create_task**
> Dict[str, object] workspace_create_task(org, workspace, request_body)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_create_task(org, workspace, request_body)
        print("The response of TasksApi->workspace_create_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_create_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**201** | Created |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_create_task_alias**
> Dict[str, object] workspace_create_task_alias(org, workspace, request_body)

Renderer-compat alias for POST /tasks.

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Renderer-compat alias for POST /tasks.
        api_response = api_instance.workspace_create_task_alias(org, workspace, request_body)
        print("The response of TasksApi->workspace_create_task_alias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_create_task_alias: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**201** | Created |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_delete_task**
> workspace_delete_task(org, workspace, id)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_delete_task(org, workspace, id)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_delete_task: %s\n" % e)
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
**204** | Deleted |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_task**
> Dict[str, object] workspace_get_task(org, workspace, id)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_task(org, workspace, id)
        print("The response of TasksApi->workspace_get_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_get_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
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
**200** | Task |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_task_providers**
> Dict[str, object] workspace_list_task_providers(org, workspace)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_task_providers(org, workspace)
        print("The response of TasksApi->workspace_list_task_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_list_task_providers: %s\n" % e)
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
**200** | Providers |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_tasks**
> Dict[str, object] workspace_list_tasks(org, workspace)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_tasks(org, workspace)
        print("The response of TasksApi->workspace_list_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_list_tasks: %s\n" % e)
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
**200** | Tasks |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_tasks_alias**
> Dict[str, object] workspace_list_tasks_alias(org, workspace)

Renderer-compat alias for /tasks.

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        # Renderer-compat alias for /tasks.
        api_response = api_instance.workspace_list_tasks_alias(org, workspace)
        print("The response of TasksApi->workspace_list_tasks_alias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_list_tasks_alias: %s\n" % e)
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
**200** | Tasks |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_update_task**
> Dict[str, object] workspace_update_task(org, workspace, id, request_body)

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_update_task(org, workspace, id, request_body)
        print("The response of TasksApi->workspace_update_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_update_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **id** | **str**|  | 
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
**200** | Updated |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_update_task_alias**
> Dict[str, object] workspace_update_task_alias(org, workspace, id, request_body)

Renderer-compat alias for PATCH /tasks/{id}.

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
    api_instance = spatio.TasksApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Renderer-compat alias for PATCH /tasks/{id}.
        api_response = api_instance.workspace_update_task_alias(org, workspace, id, request_body)
        print("The response of TasksApi->workspace_update_task_alias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling TasksApi->workspace_update_task_alias: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **id** | **str**|  | 
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
**200** | Updated |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

