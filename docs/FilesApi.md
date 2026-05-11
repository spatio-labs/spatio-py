# spatio.FilesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_delete_files**](FilesApi.md#bulk_delete_files) | **POST** /v1/files/delete | Delete multiple files in one call.
[**bulk_move_files**](FilesApi.md#bulk_move_files) | **POST** /v1/files/move | Move multiple files to a target folder.
[**commit_chunked_upload**](FilesApi.md#commit_chunked_upload) | **POST** /v1/files/upload/chunked/commit | Finalize a chunked-upload session and create the file row.
[**create_file_folder**](FilesApi.md#create_file_folder) | **POST** /v1/files/folders | Create a folder.
[**delete_file**](FilesApi.md#delete_file) | **DELETE** /v1/files/{id} | Delete a file.
[**extract_file_text**](FilesApi.md#extract_file_text) | **GET** /v1/files/{id}/extract-text | Extract text content from a PDF (or other supported file).
[**get_chunked_file_manifest**](FilesApi.md#get_chunked_file_manifest) | **GET** /v1/files/{id}/manifest | Fetch the block manifest for a chunked-uploaded file.
[**get_file**](FilesApi.md#get_file) | **GET** /v1/files/{id} | Fetch one file&#39;s metadata.
[**get_file_download_url**](FilesApi.md#get_file_download_url) | **GET** /v1/files/{id}/download | Mint a fresh signed download URL.
[**init_chunked_upload**](FilesApi.md#init_chunked_upload) | **POST** /v1/files/upload/chunked/init | Begin a content-addressed chunked upload session.
[**list_file_folders**](FilesApi.md#list_file_folders) | **GET** /v1/files/folders | List folders across connected file providers.
[**list_files**](FilesApi.md#list_files) | **GET** /v1/files | List files across connected file providers.
[**list_files_and_folders**](FilesApi.md#list_files_and_folders) | **GET** /v1/files/list | Aggregate list of files + folders for renderer file-browser views.
[**move_file**](FilesApi.md#move_file) | **POST** /v1/files/{id}/move | Move a single file to a target folder.
[**search_files**](FilesApi.md#search_files) | **GET** /v1/files/search | Substring-match search across the caller&#39;s files.
[**update_file**](FilesApi.md#update_file) | **PATCH** /v1/files/{id} | Update a file&#39;s metadata (name, folder, custom fields).
[**upload_chunked_block**](FilesApi.md#upload_chunked_block) | **POST** /v1/files/upload/chunked/blocks | Upload one block for an open chunked-upload session.
[**upload_file**](FilesApi.md#upload_file) | **POST** /v1/files/upload | Upload a file via multipart form.
[**upload_file_base64**](FilesApi.md#upload_file_base64) | **POST** /v1/files/upload/base64 | Upload a file via JSON with base64-encoded content.
[**workspace_commit_chunked_upload**](FilesApi.md#workspace_commit_chunked_upload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/commit | Workspace-scoped chunked-upload commit (RBAC-protected).
[**workspace_create_file_folder**](FilesApi.md#workspace_create_file_folder) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped create-folder (RBAC-protected).
[**workspace_delete_file**](FilesApi.md#workspace_delete_file) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped delete-file.
[**workspace_get_file**](FilesApi.md#workspace_get_file) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped get-file.
[**workspace_get_file_download**](FilesApi.md#workspace_get_file_download) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/download | Workspace-scoped signed-download URL.
[**workspace_get_file_manifest**](FilesApi.md#workspace_get_file_manifest) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/manifest | Workspace-scoped chunked-file manifest.
[**workspace_init_chunked_upload**](FilesApi.md#workspace_init_chunked_upload) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/init | Workspace-scoped chunked-upload init (RBAC-protected).
[**workspace_list_file_folders**](FilesApi.md#workspace_list_file_folders) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files/folders | Workspace-scoped list-folders (RBAC-protected).
[**workspace_list_files**](FilesApi.md#workspace_list_files) | **GET** /v1/organizations/{org}/workspaces/{workspace}/files | Workspace-scoped list-files (RBAC-protected).
[**workspace_move_file**](FilesApi.md#workspace_move_file) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/{id}/move | Workspace-scoped move-file.
[**workspace_update_file**](FilesApi.md#workspace_update_file) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/files/{id} | Workspace-scoped update-file.
[**workspace_upload_chunked_block**](FilesApi.md#workspace_upload_chunked_block) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/chunked/blocks | Workspace-scoped chunked-upload block (RBAC-protected).
[**workspace_upload_file**](FilesApi.md#workspace_upload_file) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload | Workspace-scoped multipart upload (RBAC-protected).
[**workspace_upload_file_base64**](FilesApi.md#workspace_upload_file_base64) | **POST** /v1/organizations/{org}/workspaces/{workspace}/files/upload/base64 | Workspace-scoped base64 upload (RBAC-protected).


# **bulk_delete_files**
> BulkFilesResponse bulk_delete_files(bulk_delete_files_request)

Delete multiple files in one call.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_delete_files_request import BulkDeleteFilesRequest
from spatio.models.bulk_files_response import BulkFilesResponse
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
    api_instance = spatio.FilesApi(api_client)
    bulk_delete_files_request = spatio.BulkDeleteFilesRequest() # BulkDeleteFilesRequest | 

    try:
        # Delete multiple files in one call.
        api_response = api_instance.bulk_delete_files(bulk_delete_files_request)
        print("The response of FilesApi->bulk_delete_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->bulk_delete_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_delete_files_request** | [**BulkDeleteFilesRequest**](BulkDeleteFilesRequest.md)|  | 

### Return type

[**BulkFilesResponse**](BulkFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Partial-success envelope. |  -  |
**400** | Body missing or empty. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **bulk_move_files**
> BulkFilesResponse bulk_move_files(bulk_move_files_request)

Move multiple files to a target folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_files_response import BulkFilesResponse
from spatio.models.bulk_move_files_request import BulkMoveFilesRequest
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
    api_instance = spatio.FilesApi(api_client)
    bulk_move_files_request = spatio.BulkMoveFilesRequest() # BulkMoveFilesRequest | 

    try:
        # Move multiple files to a target folder.
        api_response = api_instance.bulk_move_files(bulk_move_files_request)
        print("The response of FilesApi->bulk_move_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->bulk_move_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_move_files_request** | [**BulkMoveFilesRequest**](BulkMoveFilesRequest.md)|  | 

### Return type

[**BulkFilesResponse**](BulkFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Partial-success envelope. |  -  |
**400** | Body missing or empty. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **commit_chunked_upload**
> CommitChunkedUploadResponse commit_chunked_upload(commit_chunked_upload_request)

Finalize a chunked-upload session and create the file row.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.commit_chunked_upload_request import CommitChunkedUploadRequest
from spatio.models.commit_chunked_upload_response import CommitChunkedUploadResponse
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
    api_instance = spatio.FilesApi(api_client)
    commit_chunked_upload_request = spatio.CommitChunkedUploadRequest() # CommitChunkedUploadRequest | 

    try:
        # Finalize a chunked-upload session and create the file row.
        api_response = api_instance.commit_chunked_upload(commit_chunked_upload_request)
        print("The response of FilesApi->commit_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->commit_chunked_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **commit_chunked_upload_request** | [**CommitChunkedUploadRequest**](CommitChunkedUploadRequest.md)|  | 

### Return type

[**CommitChunkedUploadResponse**](CommitChunkedUploadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | File created. |  -  |
**400** | Unknown session or missing blocks. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_file_folder**
> Folder create_file_folder(create_folder_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)

Create a folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_folder_request import CreateFolderRequest
from spatio.models.folder import Folder
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
    api_instance = spatio.FilesApi(api_client)
    create_folder_request = spatio.CreateFolderRequest() # CreateFolderRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a folder.
        api_response = api_instance.create_file_folder(create_folder_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->create_file_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->create_file_folder: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_folder_request** | [**CreateFolderRequest**](CreateFolderRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Folder**](Folder.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Folder created. |  -  |
**400** | Invalid body or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_file**
> delete_file(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a file.

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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a file.
        api_instance.delete_file(id, account_id=account_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling FilesApi->delete_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

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
**204** | File deleted. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extract_file_text**
> ExtractTextResult extract_file_text(id, account_id=account_id, x_workspace_id=x_workspace_id, page_start=page_start, page_end=page_end, max_chars=max_chars)

Extract text content from a PDF (or other supported file).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.extract_text_result import ExtractTextResult
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    page_start = 56 # int |  (optional)
    page_end = 56 # int |  (optional)
    max_chars = 56 # int | Truncation limit; sets `truncated: true` when hit. (optional)

    try:
        # Extract text content from a PDF (or other supported file).
        api_response = api_instance.extract_file_text(id, account_id=account_id, x_workspace_id=x_workspace_id, page_start=page_start, page_end=page_end, max_chars=max_chars)
        print("The response of FilesApi->extract_file_text:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->extract_file_text: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **page_start** | **int**|  | [optional] 
 **page_end** | **int**|  | [optional] 
 **max_chars** | **int**| Truncation limit; sets &#x60;truncated: true&#x60; when hit. | [optional] 

### Return type

[**ExtractTextResult**](ExtractTextResult.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Extracted text. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |
**422** | File type isn&#39;t supported for extraction. &#x60;code: extraction_unsupported&#x60; is reserved.  |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_chunked_file_manifest**
> ChunkedFileManifest get_chunked_file_manifest(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch the block manifest for a chunked-uploaded file.

Only meaningful for files uploaded via `upload/chunked/*`.
Files uploaded via `upload` or `upload/base64` return `404`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.chunked_file_manifest import ChunkedFileManifest
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch the block manifest for a chunked-uploaded file.
        api_response = api_instance.get_chunked_file_manifest(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->get_chunked_file_manifest:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->get_chunked_file_manifest: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**ChunkedFileManifest**](ChunkedFileManifest.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Block manifest. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found or not chunked-uploaded. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_file**
> SpatioFile get_file(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one file's metadata.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.spatio_file import SpatioFile
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one file's metadata.
        api_response = api_instance.get_file(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->get_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->get_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The file. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_file_download_url**
> DownloadFileResponse get_file_download_url(id, account_id=account_id, x_workspace_id=x_workspace_id)

Mint a fresh signed download URL.

Returns a JSON envelope with a pre-signed URL pointing at the
backing storage. Clients follow the URL — the platform does
not stream bytes through itself.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.download_file_response import DownloadFileResponse
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Mint a fresh signed download URL.
        api_response = api_instance.get_file_download_url(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->get_file_download_url:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->get_file_download_url: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**DownloadFileResponse**](DownloadFileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Download envelope. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **init_chunked_upload**
> InitChunkedUploadResponse init_chunked_upload(init_chunked_upload_request)

Begin a content-addressed chunked upload session.

Client computes per-block hashes ahead of time and submits the
list. The server replies with which blocks need uploading vs.
already-on-server (deduplicated). Subsequent calls upload the
missing blocks via `uploadChunkedBlock`, then `commit`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.init_chunked_upload_request import InitChunkedUploadRequest
from spatio.models.init_chunked_upload_response import InitChunkedUploadResponse
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
    api_instance = spatio.FilesApi(api_client)
    init_chunked_upload_request = spatio.InitChunkedUploadRequest() # InitChunkedUploadRequest | 

    try:
        # Begin a content-addressed chunked upload session.
        api_response = api_instance.init_chunked_upload(init_chunked_upload_request)
        print("The response of FilesApi->init_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->init_chunked_upload: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **init_chunked_upload_request** | [**InitChunkedUploadRequest**](InitChunkedUploadRequest.md)|  | 

### Return type

[**InitChunkedUploadResponse**](InitChunkedUploadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session opened. |  -  |
**400** | Invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_file_folders**
> FolderListEnvelope list_file_folders(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, parent_id=parent_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset)

List folders across connected file providers.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.folder_list_envelope import FolderListEnvelope
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
    api_instance = spatio.FilesApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    parent_id = 'parent_id_example' # str | Filter to children of this folder. Omit for root. (optional)
    workspace_id = 'workspace_id_example' # str |  (optional)
    organization_id = 'organization_id_example' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List folders across connected file providers.
        api_response = api_instance.list_file_folders(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, parent_id=parent_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset)
        print("The response of FilesApi->list_file_folders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->list_file_folders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **parent_id** | **str**| Filter to children of this folder. Omit for root. | [optional] 
 **workspace_id** | **str**|  | [optional] 
 **organization_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**FolderListEnvelope**](FolderListEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Fan-out folder list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_files**
> FileListEnvelope list_files(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset, sort_by=sort_by, sort_order=sort_order)

List files across connected file providers.

Fan-out list. Returns files from every connected file provider
unless filtered by `?accountId=` or `?provider=`. Folder
contents are scoped via `?folderId=`; omit for account root.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.file_list_envelope import FileListEnvelope
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
    api_instance = spatio.FilesApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    folder_id = 'folder_id_example' # str | Filter to one folder. Omit for the account root. (optional)
    workspace_id = 'workspace_id_example' # str |  (optional)
    organization_id = 'organization_id_example' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)
    sort_by = 'created_at' # str | Provider-dependent. Common values: `created_at`, `name`, `size`. (optional) (default to 'created_at')
    sort_order = DESC # str |  (optional) (default to DESC)

    try:
        # List files across connected file providers.
        api_response = api_instance.list_files(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset, sort_by=sort_by, sort_order=sort_order)
        print("The response of FilesApi->list_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->list_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **folder_id** | **str**| Filter to one folder. Omit for the account root. | [optional] 
 **workspace_id** | **str**|  | [optional] 
 **organization_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]
 **sort_by** | **str**| Provider-dependent. Common values: &#x60;created_at&#x60;, &#x60;name&#x60;, &#x60;size&#x60;. | [optional] [default to &#39;created_at&#39;]
 **sort_order** | **str**|  | [optional] [default to DESC]

### Return type

[**FileListEnvelope**](FileListEnvelope.md)

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

# **list_files_and_folders**
> FilesAndFoldersResponse list_files_and_folders(account_id=account_id, provider=provider, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset, sort_by=sort_by, sort_order=sort_order)

Aggregate list of files + folders for renderer file-browser views.

Calls `listFiles` and `listFileFolders` in parallel and merges
the results. Saves a round-trip when the UI shows both
side-by-side.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.files_and_folders_response import FilesAndFoldersResponse
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
    api_instance = spatio.FilesApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    folder_id = 'folder_id_example' # str | Filter to one folder. Omit for the account root. (optional)
    workspace_id = 'workspace_id_example' # str |  (optional)
    organization_id = 'organization_id_example' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)
    sort_by = 'sort_by_example' # str |  (optional)
    sort_order = 'sort_order_example' # str |  (optional)

    try:
        # Aggregate list of files + folders for renderer file-browser views.
        api_response = api_instance.list_files_and_folders(account_id=account_id, provider=provider, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset, sort_by=sort_by, sort_order=sort_order)
        print("The response of FilesApi->list_files_and_folders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->list_files_and_folders: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **folder_id** | **str**| Filter to one folder. Omit for the account root. | [optional] 
 **workspace_id** | **str**|  | [optional] 
 **organization_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]
 **sort_by** | **str**|  | [optional] 
 **sort_order** | **str**|  | [optional] 

### Return type

[**FilesAndFoldersResponse**](FilesAndFoldersResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Aggregated &#x60;{files, folders, accounts}&#x60; envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **move_file**
> MoveFileResponse move_file(id, move_file_request, account_id=account_id, x_workspace_id=x_workspace_id)

Move a single file to a target folder.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.move_file_request import MoveFileRequest
from spatio.models.move_file_response import MoveFileResponse
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    move_file_request = spatio.MoveFileRequest() # MoveFileRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Move a single file to a target folder.
        api_response = api_instance.move_file(id, move_file_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->move_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->move_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **move_file_request** | [**MoveFileRequest**](MoveFileRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**MoveFileResponse**](MoveFileResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Move ack. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_files**
> SearchFilesResponse search_files(query, account_id=account_id, provider=provider, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset)

Substring-match search across the caller's files.

In-memory search — the platform lists up to ~500 files and
filters locally on `name` (case-insensitive substring). Not
suitable for global search across very large file libraries.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.search_files_response import SearchFilesResponse
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
    api_instance = spatio.FilesApi(api_client)
    query = 'query_example' # str | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    folder_id = 'folder_id_example' # str | Filter to one folder. Omit for the account root. (optional)
    workspace_id = 'workspace_id_example' # str |  (optional)
    organization_id = 'organization_id_example' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # Substring-match search across the caller's files.
        api_response = api_instance.search_files(query, account_id=account_id, provider=provider, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, limit=limit, offset=offset)
        print("The response of FilesApi->search_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->search_files: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **query** | **str**|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **folder_id** | **str**| Filter to one folder. Omit for the account root. | [optional] 
 **workspace_id** | **str**|  | [optional] 
 **organization_id** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**SearchFilesResponse**](SearchFilesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Filtered file list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_file**
> SpatioFile update_file(id, update_file_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a file's metadata (name, folder, custom fields).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.spatio_file import SpatioFile
from spatio.models.update_file_request import UpdateFileRequest
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
    api_instance = spatio.FilesApi(api_client)
    id = 'id_example' # str | File id.
    update_file_request = spatio.UpdateFileRequest() # UpdateFileRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a file's metadata (name, folder, custom fields).
        api_response = api_instance.update_file(id, update_file_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of FilesApi->update_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->update_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| File id. | 
 **update_file_request** | [**UpdateFileRequest**](UpdateFileRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated file. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | File not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_chunked_block**
> UploadChunkedBlockResponse upload_chunked_block(session_id, block_hash, block, block_index=block_index)

Upload one block for an open chunked-upload session.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.upload_chunked_block_response import UploadChunkedBlockResponse
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
    api_instance = spatio.FilesApi(api_client)
    session_id = 'session_id_example' # str | 
    block_hash = 'block_hash_example' # str | 
    block = None # bytes | 
    block_index = 56 # int |  (optional)

    try:
        # Upload one block for an open chunked-upload session.
        api_response = api_instance.upload_chunked_block(session_id, block_hash, block, block_index=block_index)
        print("The response of FilesApi->upload_chunked_block:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->upload_chunked_block: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **session_id** | **str**|  | 
 **block_hash** | **str**|  | 
 **block** | **bytes**|  | 
 **block_index** | **int**|  | [optional] 

### Return type

[**UploadChunkedBlockResponse**](UploadChunkedBlockResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Block accepted. |  -  |
**400** | Missing fields, unknown session, or hash mismatch. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_file**
> SpatioFile upload_file(file, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, account_id=account_id)

Upload a file via multipart form.

Multipart upload. Form field `file` carries the binary;
auxiliary form fields scope the upload (`folderId`,
`workspaceId`, `organizationId`, `accountId`). Max body size
is currently 100 MB.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.spatio_file import SpatioFile
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
    api_instance = spatio.FilesApi(api_client)
    file = None # bytes | File bytes (multipart form field name `file`).
    folder_id = 'folder_id_example' # str |  (optional)
    workspace_id = 'workspace_id_example' # str |  (optional)
    organization_id = 'organization_id_example' # str |  (optional)
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Upload a file via multipart form.
        api_response = api_instance.upload_file(file, folder_id=folder_id, workspace_id=workspace_id, organization_id=organization_id, account_id=account_id)
        print("The response of FilesApi->upload_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->upload_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **bytes**| File bytes (multipart form field name &#x60;file&#x60;). | 
 **folder_id** | **str**|  | [optional] 
 **workspace_id** | **str**|  | [optional] 
 **organization_id** | **str**|  | [optional] 
 **account_id** | **str**|  | [optional] 

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | File created. |  -  |
**400** | Multipart parse error, ambiguous account, or no file provider connected.  |  -  |
**401** | Caller is not authenticated. |  -  |
**402** | Storage quota exceeded. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upload_file_base64**
> SpatioFile upload_file_base64(upload_file_base64_request)

Upload a file via JSON with base64-encoded content.

Equivalent to `uploadFile` for clients that can't post
multipart bodies (e.g. browser fetch with strict CSP).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.spatio_file import SpatioFile
from spatio.models.upload_file_base64_request import UploadFileBase64Request
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
    api_instance = spatio.FilesApi(api_client)
    upload_file_base64_request = spatio.UploadFileBase64Request() # UploadFileBase64Request | 

    try:
        # Upload a file via JSON with base64-encoded content.
        api_response = api_instance.upload_file_base64(upload_file_base64_request)
        print("The response of FilesApi->upload_file_base64:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->upload_file_base64: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **upload_file_base64_request** | [**UploadFileBase64Request**](UploadFileBase64Request.md)|  | 

### Return type

[**SpatioFile**](SpatioFile.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | File created. |  -  |
**400** | Invalid body, ambiguous account, or no provider. |  -  |
**401** | Caller is not authenticated. |  -  |
**402** | Storage quota exceeded. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_commit_chunked_upload**
> Dict[str, object] workspace_commit_chunked_upload(org, workspace, request_body)

Workspace-scoped chunked-upload commit (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped chunked-upload commit (RBAC-protected).
        api_response = api_instance.workspace_commit_chunked_upload(org, workspace, request_body)
        print("The response of FilesApi->workspace_commit_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_commit_chunked_upload: %s\n" % e)
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
**200** | Committed |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_create_file_folder**
> Dict[str, object] workspace_create_file_folder(org, workspace, request_body)

Workspace-scoped create-folder (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped create-folder (RBAC-protected).
        api_response = api_instance.workspace_create_file_folder(org, workspace, request_body)
        print("The response of FilesApi->workspace_create_file_folder:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_create_file_folder: %s\n" % e)
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

# **workspace_delete_file**
> workspace_delete_file(org, workspace, id)

Workspace-scoped delete-file.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        # Workspace-scoped delete-file.
        api_instance.workspace_delete_file(org, workspace, id)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_delete_file: %s\n" % e)
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

# **workspace_get_file**
> Dict[str, object] workspace_get_file(org, workspace, id)

Workspace-scoped get-file.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        # Workspace-scoped get-file.
        api_response = api_instance.workspace_get_file(org, workspace, id)
        print("The response of FilesApi->workspace_get_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_get_file: %s\n" % e)
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
**200** | File |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_file_download**
> Dict[str, object] workspace_get_file_download(org, workspace, id)

Workspace-scoped signed-download URL.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        # Workspace-scoped signed-download URL.
        api_response = api_instance.workspace_get_file_download(org, workspace, id)
        print("The response of FilesApi->workspace_get_file_download:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_get_file_download: %s\n" % e)
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
**200** | Download URL envelope |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_file_manifest**
> Dict[str, object] workspace_get_file_manifest(org, workspace, id)

Workspace-scoped chunked-file manifest.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        # Workspace-scoped chunked-file manifest.
        api_response = api_instance.workspace_get_file_manifest(org, workspace, id)
        print("The response of FilesApi->workspace_get_file_manifest:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_get_file_manifest: %s\n" % e)
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
**200** | Manifest |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_init_chunked_upload**
> Dict[str, object] workspace_init_chunked_upload(org, workspace, request_body)

Workspace-scoped chunked-upload init (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped chunked-upload init (RBAC-protected).
        api_response = api_instance.workspace_init_chunked_upload(org, workspace, request_body)
        print("The response of FilesApi->workspace_init_chunked_upload:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_init_chunked_upload: %s\n" % e)
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
**200** | Init result |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_file_folders**
> Dict[str, object] workspace_list_file_folders(org, workspace)

Workspace-scoped list-folders (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        # Workspace-scoped list-folders (RBAC-protected).
        api_response = api_instance.workspace_list_file_folders(org, workspace)
        print("The response of FilesApi->workspace_list_file_folders:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_list_file_folders: %s\n" % e)
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
**200** | Folder envelope |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_files**
> Dict[str, object] workspace_list_files(org, workspace)

Workspace-scoped list-files (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        # Workspace-scoped list-files (RBAC-protected).
        api_response = api_instance.workspace_list_files(org, workspace)
        print("The response of FilesApi->workspace_list_files:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_list_files: %s\n" % e)
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
**200** | File envelope |  -  |
**401** | Caller is not authenticated |  -  |
**403** | Caller lacks workspace files:read |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_move_file**
> Dict[str, object] workspace_move_file(org, workspace, id, request_body)

Workspace-scoped move-file.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped move-file.
        api_response = api_instance.workspace_move_file(org, workspace, id, request_body)
        print("The response of FilesApi->workspace_move_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_move_file: %s\n" % e)
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
**200** | Moved |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_update_file**
> Dict[str, object] workspace_update_file(org, workspace, id, request_body)

Workspace-scoped update-file.

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped update-file.
        api_response = api_instance.workspace_update_file(org, workspace, id, request_body)
        print("The response of FilesApi->workspace_update_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_update_file: %s\n" % e)
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

# **workspace_upload_chunked_block**
> Dict[str, object] workspace_upload_chunked_block(org, workspace, body)

Workspace-scoped chunked-upload block (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    body = None # bytes | 

    try:
        # Workspace-scoped chunked-upload block (RBAC-protected).
        api_response = api_instance.workspace_upload_chunked_block(org, workspace, body)
        print("The response of FilesApi->workspace_upload_chunked_block:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_upload_chunked_block: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **body** | **bytes**|  | 

### Return type

**Dict[str, object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/octet-stream
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Block uploaded |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_upload_file**
> Dict[str, object] workspace_upload_file(org, workspace, file=file)

Workspace-scoped multipart upload (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    file = None # bytes |  (optional)

    try:
        # Workspace-scoped multipart upload (RBAC-protected).
        api_response = api_instance.workspace_upload_file(org, workspace, file=file)
        print("The response of FilesApi->workspace_upload_file:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_upload_file: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **file** | **bytes**|  | [optional] 

### Return type

**Dict[str, object]**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Uploaded |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_upload_file_base64**
> Dict[str, object] workspace_upload_file_base64(org, workspace, request_body)

Workspace-scoped base64 upload (RBAC-protected).

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
    api_instance = spatio.FilesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Workspace-scoped base64 upload (RBAC-protected).
        api_response = api_instance.workspace_upload_file_base64(org, workspace, request_body)
        print("The response of FilesApi->workspace_upload_file_base64:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling FilesApi->workspace_upload_file_base64: %s\n" % e)
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
**201** | Uploaded |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

