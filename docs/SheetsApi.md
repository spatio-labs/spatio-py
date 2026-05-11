# spatio.SheetsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_sheet**](SheetsApi.md#create_sheet) | **POST** /v1/sheets | Create a sheet.
[**create_sheet_row**](SheetsApi.md#create_sheet_row) | **POST** /v1/sheets/{id}/rows | Insert a row.
[**delete_sheet**](SheetsApi.md#delete_sheet) | **DELETE** /v1/sheets/{id} | Delete a sheet.
[**delete_sheet_row**](SheetsApi.md#delete_sheet_row) | **DELETE** /v1/sheets/{id}/rows/{rowIndex} | Delete a row.
[**get_sheet**](SheetsApi.md#get_sheet) | **GET** /v1/sheets/{id} | Fetch one sheet.
[**list_sheet_rows**](SheetsApi.md#list_sheet_rows) | **GET** /v1/sheets/{id}/rows | List rows in a sheet.
[**list_sheets**](SheetsApi.md#list_sheets) | **GET** /v1/sheets | List sheets across connected accounts.
[**update_sheet**](SheetsApi.md#update_sheet) | **PATCH** /v1/sheets/{id} | Update a sheet (partial).
[**update_sheet_cell**](SheetsApi.md#update_sheet_cell) | **PATCH** /v1/sheets/{id}/rows/{rowIndex}/cells/{column} | Update a single cell.
[**update_sheet_row**](SheetsApi.md#update_sheet_row) | **PATCH** /v1/sheets/{id}/rows/{rowIndex} | Update a row (sparse).


# **create_sheet**
> Sheet create_sheet(create_sheet_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)

Create a sheet.

Creates a new sheet under the target account. Target resolution
mirrors `POST /v1/notes`: body `accountId` → `?accountId=` →
body `provider` → `?provider=` → caller's single connected
account (errors with `ambiguous_account` if more than one is
connected and no selector is supplied).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_sheet_request import CreateSheetRequest
from spatio.models.sheet import Sheet
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
    api_instance = spatio.SheetsApi(api_client)
    create_sheet_request = spatio.CreateSheetRequest() # CreateSheetRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a sheet.
        api_response = api_instance.create_sheet(create_sheet_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->create_sheet:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->create_sheet: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_sheet_request** | [**CreateSheetRequest**](CreateSheetRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Sheet created. |  -  |
**400** | Invalid body, ambiguous account (&#x60;code: ambiguous_account&#x60;), or no sheets provider connected (&#x60;code: no_sheets_provider&#x60;).  |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_sheet_row**
> Row create_sheet_row(id, create_row_request, account_id=account_id, x_workspace_id=x_workspace_id)

Insert a row.

Inserts a row at `index` (zero-based) or appends to the end
when `index` is omitted.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_row_request import CreateRowRequest
from spatio.models.row import Row
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    create_row_request = spatio.CreateRowRequest() # CreateRowRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Insert a row.
        api_response = api_instance.create_sheet_row(id, create_row_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->create_sheet_row:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->create_sheet_row: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **create_row_request** | [**CreateRowRequest**](CreateRowRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Row**](Row.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Row created. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_sheet**
> SuccessFlag delete_sheet(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a sheet.

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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a sheet.
        api_response = api_instance.delete_sheet(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->delete_sheet:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->delete_sheet: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
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
**404** | Sheet not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_sheet_row**
> SuccessFlag delete_sheet_row(id, row_index, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a row.

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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    row_index = 56 # int | Zero-based row index.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a row.
        api_response = api_instance.delete_sheet_row(id, row_index, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->delete_sheet_row:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->delete_sheet_row: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **row_index** | **int**| Zero-based row index. | 
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
**400** | Missing id or invalid row index. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet or row not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_sheet**
> Sheet get_sheet(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one sheet.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.sheet import Sheet
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one sheet.
        api_response = api_instance.get_sheet(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->get_sheet:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->get_sheet: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The sheet. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sheet_rows**
> RowList list_sheet_rows(id, account_id=account_id, x_workspace_id=x_workspace_id, limit=limit, offset=offset)

List rows in a sheet.

Single-account row list. Unlike `GET /v1/sheets`, row listing
always targets the one account that owns the sheet, so the
response is a plain `{ rows, total }` rather than a fan-out
envelope.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.row_list import RowList
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 100 # int |  (optional) (default to 100)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List rows in a sheet.
        api_response = api_instance.list_sheet_rows(id, account_id=account_id, x_workspace_id=x_workspace_id, limit=limit, offset=offset)
        print("The response of SheetsApi->list_sheet_rows:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->list_sheet_rows: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **limit** | **int**|  | [optional] [default to 100]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**RowList**](RowList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Row list. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sheets**
> SheetListEnvelope list_sheets(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, limit=limit, offset=offset)

List sheets across connected accounts.

Fan-out list. Returns every sheet visible to the caller across
every connected sheets provider, paginated by `limit` / `offset`.
Pass `?accountId=` or `?provider=` to scope to a single source.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.sheet_list_envelope import SheetListEnvelope
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
    api_instance = spatio.SheetsApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List sheets across connected accounts.
        api_response = api_instance.list_sheets(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, limit=limit, offset=offset)
        print("The response of SheetsApi->list_sheets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->list_sheets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**SheetListEnvelope**](SheetListEnvelope.md)

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

# **update_sheet**
> Sheet update_sheet(id, update_sheet_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a sheet (partial).

Partial update of sheet metadata. The renderer also calls this
via `PUT /v1/sheets/{id}` for autosave parity; both verbs invoke
the same handler. Per-cell and per-row mutations live on their
dedicated endpoints, not here.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.sheet import Sheet
from spatio.models.update_sheet_request import UpdateSheetRequest
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    update_sheet_request = spatio.UpdateSheetRequest() # UpdateSheetRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a sheet (partial).
        api_response = api_instance.update_sheet(id, update_sheet_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->update_sheet:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->update_sheet: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **update_sheet_request** | [**UpdateSheetRequest**](UpdateSheetRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Sheet**](Sheet.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated sheet. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sheet_cell**
> Cell update_sheet_cell(id, row_index, column, update_cell_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a single cell.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.cell import Cell
from spatio.models.update_cell_request import UpdateCellRequest
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    row_index = 56 # int | Zero-based row index.
    column = 'column_example' # str | Column identifier. Provider-specific — usually a letter (`A`, `AB`) for spreadsheet providers or a column key string for structured providers. 
    update_cell_request = spatio.UpdateCellRequest() # UpdateCellRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a single cell.
        api_response = api_instance.update_sheet_cell(id, row_index, column, update_cell_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->update_sheet_cell:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->update_sheet_cell: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **row_index** | **int**| Zero-based row index. | 
 **column** | **str**| Column identifier. Provider-specific — usually a letter (&#x60;A&#x60;, &#x60;AB&#x60;) for spreadsheet providers or a column key string for structured providers.  | 
 **update_cell_request** | [**UpdateCellRequest**](UpdateCellRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Cell**](Cell.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated cell. |  -  |
**400** | Invalid body, missing id, invalid row index, or missing column.  |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet, row, or cell not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_sheet_row**
> Row update_sheet_row(id, row_index, update_row_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a row (sparse).

Sparse update — keys present in `cells` overwrite that column;
keys absent are preserved.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.row import Row
from spatio.models.update_row_request import UpdateRowRequest
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
    api_instance = spatio.SheetsApi(api_client)
    id = 'id_example' # str | Sheet id.
    row_index = 56 # int | Zero-based row index.
    update_row_request = spatio.UpdateRowRequest() # UpdateRowRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a row (sparse).
        api_response = api_instance.update_sheet_row(id, row_index, update_row_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SheetsApi->update_sheet_row:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SheetsApi->update_sheet_row: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Sheet id. | 
 **row_index** | **int**| Zero-based row index. | 
 **update_row_request** | [**UpdateRowRequest**](UpdateRowRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Row**](Row.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated row. |  -  |
**400** | Invalid body, missing id, or invalid row index. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Sheet or row not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

