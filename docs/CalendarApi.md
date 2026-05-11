# spatio.CalendarApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_calendar_event**](CalendarApi.md#create_calendar_event) | **POST** /v1/calendar/events | Create a calendar event.
[**delete_calendar_event**](CalendarApi.md#delete_calendar_event) | **DELETE** /v1/calendar/events/{id} | Delete an event.
[**get_calendar_capabilities**](CalendarApi.md#get_calendar_capabilities) | **GET** /v1/calendar/capabilities | Per-account capability flags.
[**get_calendar_event**](CalendarApi.md#get_calendar_event) | **GET** /v1/calendar/events/{id} | Fetch one event.
[**list_calendar_events**](CalendarApi.md#list_calendar_events) | **GET** /v1/calendar/events | List calendar events across connected accounts.
[**list_calendar_providers**](CalendarApi.md#list_calendar_providers) | **GET** /v1/calendar/providers | List supported calendar providers.
[**sync_calendar**](CalendarApi.md#sync_calendar) | **POST** /v1/calendar/sync | Trigger a sync across connected calendar accounts.
[**update_calendar_event**](CalendarApi.md#update_calendar_event) | **PATCH** /v1/calendar/events/{id} | Update an event (sparse).
[**workspace_create_calendar_event**](CalendarApi.md#workspace_create_calendar_event) | **POST** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped create-event (RBAC-protected).
[**workspace_delete_calendar_event**](CalendarApi.md#workspace_delete_calendar_event) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 
[**workspace_get_calendar_event**](CalendarApi.md#workspace_get_calendar_event) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 
[**workspace_list_calendar_events**](CalendarApi.md#workspace_list_calendar_events) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/events | Workspace-scoped list-events (RBAC-protected).
[**workspace_list_calendar_providers**](CalendarApi.md#workspace_list_calendar_providers) | **GET** /v1/organizations/{org}/workspaces/{workspace}/calendar/providers | Workspace-scoped calendar providers.
[**workspace_update_calendar_event**](CalendarApi.md#workspace_update_calendar_event) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/calendar/events/{id} | 


# **create_calendar_event**
> CreateCalendarEvent201Response create_calendar_event(create_event_request, x_workspace_id=x_workspace_id)

Create a calendar event.

Single-account create. `account_id` is required (no auto-resolve
for write operations). Reminder array is mirrored into native
tasks under the hood; conference data is auto-attached when
`conference_type` is supplied.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_calendar_event201_response import CreateCalendarEvent201Response
from spatio.models.create_event_request import CreateEventRequest
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
    api_instance = spatio.CalendarApi(api_client)
    create_event_request = spatio.CreateEventRequest() # CreateEventRequest | 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a calendar event.
        api_response = api_instance.create_calendar_event(create_event_request, x_workspace_id=x_workspace_id)
        print("The response of CalendarApi->create_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->create_calendar_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_event_request** | [**CreateEventRequest**](CreateEventRequest.md)|  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Operation envelope. &#x60;data&#x60; is the created &#x60;Event&#x60;.  |  -  |
**400** | Invalid body or missing &#x60;account_id&#x60;. |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Provider or capability failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_calendar_event**
> CalendarOperationResult delete_calendar_event(id, account_id, x_workspace_id=x_workspace_id)

Delete an event.

Hard delete (no soft-delete / trash). Cascades to any reminder
tasks the platform created from this event.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.calendar_operation_result import CalendarOperationResult
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
    api_instance = spatio.CalendarApi(api_client)
    id = 'id_example' # str | Event id.
    account_id = 'account_id_example' # str | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete an event.
        api_response = api_instance.delete_calendar_event(id, account_id, x_workspace_id=x_workspace_id)
        print("The response of CalendarApi->delete_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->delete_calendar_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Event id. | 
 **account_id** | **str**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**CalendarOperationResult**](CalendarOperationResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Operation envelope. &#x60;metadata&#x60; carries &#x60;deleted_event_id&#x60; and &#x60;deleted_at&#x60;.  |  -  |
**400** | Missing id or account_id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Event not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_calendar_capabilities**
> CalendarCapabilitiesResponse get_calendar_capabilities(account_id)

Per-account capability flags.

Returns the capabilities the provider declares for the given
connected account. The renderer uses these to enable/disable
form fields (recurrence picker, attendee inputs, etc.).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.calendar_capabilities_response import CalendarCapabilitiesResponse
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
    api_instance = spatio.CalendarApi(api_client)
    account_id = 'account_id_example' # str | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 

    try:
        # Per-account capability flags.
        api_response = api_instance.get_calendar_capabilities(account_id)
        print("The response of CalendarApi->get_calendar_capabilities:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->get_calendar_capabilities: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | 

### Return type

[**CalendarCapabilitiesResponse**](CalendarCapabilitiesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Capabilities envelope. |  -  |
**400** | Missing account_id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Account not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_calendar_event**
> SpatioEvent get_calendar_event(id, account_id, x_workspace_id=x_workspace_id)

Fetch one event.

Requires `?account_id=` to identify the source account.
Response is the bare `Event` (not wrapped in
CalendarOperationResult — distinct from the list/create/update
shapes).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.spatio_event import SpatioEvent
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
    api_instance = spatio.CalendarApi(api_client)
    id = 'id_example' # str | Event id.
    account_id = 'account_id_example' # str | Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses `accountId`). Required for single-event operations. 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one event.
        api_response = api_instance.get_calendar_event(id, account_id, x_workspace_id=x_workspace_id)
        print("The response of CalendarApi->get_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->get_calendar_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Event id. | 
 **account_id** | **str**| Connected-account id (snake_case in this platform — the rest of the SpatioAPI uses &#x60;accountId&#x60;). Required for single-event operations.  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SpatioEvent**](SpatioEvent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The event. |  -  |
**400** | Missing id or account_id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Event not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_calendar_events**
> ListCalendarEvents200Response list_calendar_events(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, time_min=time_min, time_max=time_max, limit=limit)

List calendar events across connected accounts.

Fan-out list. Returns events across every connected calendar
provider unless filtered by `account_ids[]` or `providers[]`.
Supports the cross-platform repeated-or-comma-separated filter
syntax (`?account_ids=a&account_ids=b` or `?account_ids=a,b`).

Time bounds (`timeMin` / `timeMax`) accept both RFC3339 and
RFC3339Nano. The handler also accepts the snake_case
`time_min` / `time_max` for direct curl callers; the spec
models the camelCase form because that's what the renderer
and SDKs use.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_calendar_events200_response import ListCalendarEvents200Response
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
    api_instance = spatio.CalendarApi(api_client)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to specific connected accounts. (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to provider ids (`google-calendar`, etc.). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    time_min = '2013-10-20T19:20:30+01:00' # datetime | Inclusive lower-bound time. RFC3339 or RFC3339Nano. (optional)
    time_max = '2013-10-20T19:20:30+01:00' # datetime | Inclusive upper-bound time. (optional)
    limit = 50 # int | Max events to return per page (default 50). (optional) (default to 50)

    try:
        # List calendar events across connected accounts.
        api_response = api_instance.list_calendar_events(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, time_min=time_min, time_max=time_max, limit=limit)
        print("The response of CalendarApi->list_calendar_events:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->list_calendar_events: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to specific connected accounts. | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to provider ids (&#x60;google-calendar&#x60;, etc.). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **time_min** | **datetime**| Inclusive lower-bound time. RFC3339 or RFC3339Nano. | [optional] 
 **time_max** | **datetime**| Inclusive upper-bound time. | [optional] 
 **limit** | **int**| Max events to return per page (default 50). | [optional] [default to 50]

### Return type

[**ListCalendarEvents200Response**](ListCalendarEvents200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Operation envelope. &#x60;data&#x60; is &#x60;ListEventsData&#x60;. Per-account fetch failures appear in &#x60;errors&#x60; rather than failing the whole call.  |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Resolver or fan-out failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_calendar_providers**
> CalendarProvidersInfo list_calendar_providers()

List supported calendar providers.

Static list of provider ids the Calendar platform can connect
to. Returned regardless of which providers the caller has
actually authorized.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.calendar_providers_info import CalendarProvidersInfo
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
    api_instance = spatio.CalendarApi(api_client)

    try:
        # List supported calendar providers.
        api_response = api_instance.list_calendar_providers()
        print("The response of CalendarApi->list_calendar_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->list_calendar_providers: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**CalendarProvidersInfo**](CalendarProvidersInfo.md)

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

# **sync_calendar**
> CalendarSyncResponse sync_calendar(wait=wait)

Trigger a sync across connected calendar accounts.

Enqueues sync jobs (one per connected calendar account) and
returns immediately with the job ids. Pass `?wait=true` to
block until all jobs complete (10-second polling budget); the
response is then `200` with `waited: true` and a `timed_out`
flag if any job didn't finish in time.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.calendar_sync_response import CalendarSyncResponse
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
    api_instance = spatio.CalendarApi(api_client)
    wait = False # bool | Block until all sync jobs finish (10s timeout). (optional) (default to False)

    try:
        # Trigger a sync across connected calendar accounts.
        api_response = api_instance.sync_calendar(wait=wait)
        print("The response of CalendarApi->sync_calendar:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->sync_calendar: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **wait** | **bool**| Block until all sync jobs finish (10s timeout). | [optional] [default to False]

### Return type

[**CalendarSyncResponse**](CalendarSyncResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Synchronous completion (only when &#x60;?wait&#x3D;true&#x60;). |  -  |
**202** | Sync jobs enqueued; check the worker for completion. |  -  |
**401** | Caller is not authenticated. |  -  |
**503** | Sync queue not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_calendar_event**
> CreateCalendarEvent201Response update_calendar_event(id, update_event_request, x_workspace_id=x_workspace_id, account_id=account_id)

Update an event (sparse).

Partial update. `account_id` may be supplied in the body
(preferred) or as `?account_id=` query param — the renderer's
update path puts it in the URL while create puts it in the
body. `updates` is a free-form map; the platform's capability
gate rejects fields the provider doesn't support.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_calendar_event201_response import CreateCalendarEvent201Response
from spatio.models.update_event_request import UpdateEventRequest
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
    api_instance = spatio.CalendarApi(api_client)
    id = 'id_example' # str | Event id.
    update_event_request = spatio.UpdateEventRequest() # UpdateEventRequest | 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    account_id = 'account_id_example' # str | Optional account-id filter (snake_case). (optional)

    try:
        # Update an event (sparse).
        api_response = api_instance.update_calendar_event(id, update_event_request, x_workspace_id=x_workspace_id, account_id=account_id)
        print("The response of CalendarApi->update_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->update_calendar_event: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Event id. | 
 **update_event_request** | [**UpdateEventRequest**](UpdateEventRequest.md)|  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **account_id** | **str**| Optional account-id filter (snake_case). | [optional] 

### Return type

[**CreateCalendarEvent201Response**](CreateCalendarEvent201Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Operation envelope. &#x60;data&#x60; is the updated &#x60;Event&#x60;.  |  -  |
**400** | Invalid body, missing id, or missing account_id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Event not found. |  -  |
**500** | Provider or capability failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_create_calendar_event**
> Dict[str, object] workspace_create_calendar_event(org, workspace, request_body)

Workspace-scoped create-event (RBAC-protected).

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped create-event (RBAC-protected).
        api_response = api_instance.workspace_create_calendar_event(org, workspace, request_body)
        print("The response of CalendarApi->workspace_create_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_create_calendar_event: %s\n" % e)
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

# **workspace_delete_calendar_event**
> workspace_delete_calendar_event(org, workspace, id)

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_delete_calendar_event(org, workspace, id)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_delete_calendar_event: %s\n" % e)
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

# **workspace_get_calendar_event**
> Dict[str, object] workspace_get_calendar_event(org, workspace, id)

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_calendar_event(org, workspace, id)
        print("The response of CalendarApi->workspace_get_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_get_calendar_event: %s\n" % e)
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
**200** | Event |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_calendar_events**
> Dict[str, object] workspace_list_calendar_events(org, workspace)

Workspace-scoped list-events (RBAC-protected).

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        # Workspace-scoped list-events (RBAC-protected).
        api_response = api_instance.workspace_list_calendar_events(org, workspace)
        print("The response of CalendarApi->workspace_list_calendar_events:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_list_calendar_events: %s\n" % e)
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
**200** | Events |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_calendar_providers**
> Dict[str, object] workspace_list_calendar_providers(org, workspace)

Workspace-scoped calendar providers.

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        # Workspace-scoped calendar providers.
        api_response = api_instance.workspace_list_calendar_providers(org, workspace)
        print("The response of CalendarApi->workspace_list_calendar_providers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_list_calendar_providers: %s\n" % e)
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

# **workspace_update_calendar_event**
> Dict[str, object] workspace_update_calendar_event(org, workspace, id, request_body)

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
    api_instance = spatio.CalendarApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_update_calendar_event(org, workspace, id, request_body)
        print("The response of CalendarApi->workspace_update_calendar_event:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CalendarApi->workspace_update_calendar_event: %s\n" % e)
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

