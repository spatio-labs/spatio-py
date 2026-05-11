# spatio.MailApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_archive_emails**](MailApi.md#bulk_archive_emails) | **POST** /v1/mail/archive | Archive multiple messages (remove the INBOX label).
[**bulk_delete_emails**](MailApi.md#bulk_delete_emails) | **POST** /v1/mail/delete | Delete multiple messages in one call.
[**bulk_mark_emails_read**](MailApi.md#bulk_mark_emails_read) | **POST** /v1/mail/mark-read | Mark multiple messages read or unread in one call.
[**create_draft**](MailApi.md#create_draft) | **POST** /v1/mail/drafts | Create a draft.
[**create_email_label**](MailApi.md#create_email_label) | **POST** /v1/mail/labels | Create a label.
[**create_mail_template**](MailApi.md#create_mail_template) | **POST** /v1/mail/templates | Create a mail template.
[**delete_draft**](MailApi.md#delete_draft) | **DELETE** /v1/mail/drafts/{id} | Delete a draft.
[**delete_email**](MailApi.md#delete_email) | **DELETE** /v1/mail/email/{id} | Delete an email.
[**delete_email_label**](MailApi.md#delete_email_label) | **DELETE** /v1/mail/labels/{id} | Delete a label.
[**delete_mail_template**](MailApi.md#delete_mail_template) | **DELETE** /v1/mail/templates/{id} | Delete a mail template.
[**get_email**](MailApi.md#get_email) | **GET** /v1/mail/email/{id} | Fetch one email.
[**get_email_attachment**](MailApi.md#get_email_attachment) | **GET** /v1/mail/attachment/{messageId}/{attachmentId} | Download an attachment.
[**get_email_thread**](MailApi.md#get_email_thread) | **GET** /v1/mail/thread/{id} | Fetch a thread (the conversation a message belongs to).
[**get_mail_template**](MailApi.md#get_mail_template) | **GET** /v1/mail/templates/{id} | Fetch a mail template.
[**get_mail_thread_tracking**](MailApi.md#get_mail_thread_tracking) | **GET** /v1/mail/threads/{threadId}/tracking | Read mail-tracking events for a thread (open log, reply log, etc.).
[**instantiate_mail_template**](MailApi.md#instantiate_mail_template) | **POST** /v1/mail/templates/{id}/instantiate | Render a template with variables and return the resulting draft.
[**list_drafts**](MailApi.md#list_drafts) | **GET** /v1/mail/drafts | List drafts across connected mail accounts.
[**list_email_labels**](MailApi.md#list_email_labels) | **GET** /v1/mail/labels | List labels on the resolved mail account.
[**list_emails**](MailApi.md#list_emails) | **GET** /v1/mail/list | List emails across connected mail accounts.
[**list_mail_templates**](MailApi.md#list_mail_templates) | **GET** /v1/mail/templates | List the caller&#39;s saved mail templates.
[**reply_email**](MailApi.md#reply_email) | **POST** /v1/mail/reply | Reply to a specific email.
[**save_mail_template**](MailApi.md#save_mail_template) | **POST** /v1/mail/templates/save | Save-or-create endpoint used by the renderer&#39;s \&quot;save as template\&quot; flow. Distinct from POST /v1/mail/templates which is the strict create. 
[**search_emails**](MailApi.md#search_emails) | **GET** /v1/mail/search | Structured search across connected mail accounts.
[**send_draft**](MailApi.md#send_draft) | **POST** /v1/mail/drafts/{id}/send | Send a draft.
[**send_email**](MailApi.md#send_email) | **POST** /v1/mail/send | Send an email.
[**update_draft**](MailApi.md#update_draft) | **PUT** /v1/mail/drafts/{id} | Update a draft (full replacement of provided fields).
[**update_email**](MailApi.md#update_email) | **PATCH** /v1/mail/email/{id} | Update an email (mark read/star, add/remove labels).
[**update_mail_template**](MailApi.md#update_mail_template) | **PATCH** /v1/mail/templates/{id} | Update a mail template.
[**workspace_add_mail_message_labels**](MailApi.md#workspace_add_mail_message_labels) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/{messageId}/labels | 
[**workspace_create_mail_draft**](MailApi.md#workspace_create_mail_draft) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts | 
[**workspace_create_mail_label**](MailApi.md#workspace_create_mail_label) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/labels | 
[**workspace_delete_mail**](MailApi.md#workspace_delete_mail) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} | 
[**workspace_delete_mail_draft**](MailApi.md#workspace_delete_mail_draft) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} | 
[**workspace_delete_mail_label**](MailApi.md#workspace_delete_mail_label) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/labels/{id} | 
[**workspace_get_mail**](MailApi.md#workspace_get_mail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} | 
[**workspace_get_mail_attachment**](MailApi.md#workspace_get_mail_attachment) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/attachment/{messageId}/{attachmentId} | 
[**workspace_get_mail_by_id**](MailApi.md#workspace_get_mail_by_id) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/{id} | Workspace-scoped renderer-compat alias for mail/email/{id}.
[**workspace_get_mail_draft**](MailApi.md#workspace_get_mail_draft) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} | 
[**workspace_get_mail_thread**](MailApi.md#workspace_get_mail_thread) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/thread/{id} | 
[**workspace_list_mail**](MailApi.md#workspace_list_mail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/list | 
[**workspace_list_mail_drafts**](MailApi.md#workspace_list_mail_drafts) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts | 
[**workspace_list_mail_labels**](MailApi.md#workspace_list_mail_labels) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/labels | 
[**workspace_patch_mail**](MailApi.md#workspace_patch_mail) | **PATCH** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} | 
[**workspace_remove_mail_message_label**](MailApi.md#workspace_remove_mail_message_label) | **DELETE** /v1/organizations/{org}/workspaces/{workspace}/mail/{messageId}/labels/{labelId} | 
[**workspace_reply_mail**](MailApi.md#workspace_reply_mail) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/reply | 
[**workspace_search_mail**](MailApi.md#workspace_search_mail) | **GET** /v1/organizations/{org}/workspaces/{workspace}/mail/search | 
[**workspace_send_mail**](MailApi.md#workspace_send_mail) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/send | 
[**workspace_send_mail_draft**](MailApi.md#workspace_send_mail_draft) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id}/send | 
[**workspace_send_mail_email_alias**](MailApi.md#workspace_send_mail_email_alias) | **POST** /v1/organizations/{org}/workspaces/{workspace}/mail/email | Renderer-compat alias for /mail/send.
[**workspace_update_mail**](MailApi.md#workspace_update_mail) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/email/{id} | 
[**workspace_update_mail_draft**](MailApi.md#workspace_update_mail_draft) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/drafts/{id} | 
[**workspace_update_mail_label**](MailApi.md#workspace_update_mail_label) | **PUT** /v1/organizations/{org}/workspaces/{workspace}/mail/labels/{id} | 


# **bulk_archive_emails**
> BulkArchiveResponse bulk_archive_emails(bulk_archive_request)

Archive multiple messages (remove the INBOX label).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_archive_request import BulkArchiveRequest
from spatio.models.bulk_archive_response import BulkArchiveResponse
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
    api_instance = spatio.MailApi(api_client)
    bulk_archive_request = spatio.BulkArchiveRequest() # BulkArchiveRequest | 

    try:
        # Archive multiple messages (remove the INBOX label).
        api_response = api_instance.bulk_archive_emails(bulk_archive_request)
        print("The response of MailApi->bulk_archive_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->bulk_archive_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_archive_request** | [**BulkArchiveRequest**](BulkArchiveRequest.md)|  | 

### Return type

[**BulkArchiveResponse**](BulkArchiveResponse.md)

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

# **bulk_delete_emails**
> BulkDeleteEmailsResponse bulk_delete_emails(bulk_delete_emails_request)

Delete multiple messages in one call.

Soft-delete by default (moves to provider trash). Set
`permanent: true` for a hard delete.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_delete_emails_request import BulkDeleteEmailsRequest
from spatio.models.bulk_delete_emails_response import BulkDeleteEmailsResponse
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
    api_instance = spatio.MailApi(api_client)
    bulk_delete_emails_request = spatio.BulkDeleteEmailsRequest() # BulkDeleteEmailsRequest | 

    try:
        # Delete multiple messages in one call.
        api_response = api_instance.bulk_delete_emails(bulk_delete_emails_request)
        print("The response of MailApi->bulk_delete_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->bulk_delete_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_delete_emails_request** | [**BulkDeleteEmailsRequest**](BulkDeleteEmailsRequest.md)|  | 

### Return type

[**BulkDeleteEmailsResponse**](BulkDeleteEmailsResponse.md)

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

# **bulk_mark_emails_read**
> BulkMarkReadResponse bulk_mark_emails_read(bulk_mark_read_request)

Mark multiple messages read or unread in one call.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.bulk_mark_read_request import BulkMarkReadRequest
from spatio.models.bulk_mark_read_response import BulkMarkReadResponse
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
    api_instance = spatio.MailApi(api_client)
    bulk_mark_read_request = spatio.BulkMarkReadRequest() # BulkMarkReadRequest | 

    try:
        # Mark multiple messages read or unread in one call.
        api_response = api_instance.bulk_mark_emails_read(bulk_mark_read_request)
        print("The response of MailApi->bulk_mark_emails_read:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->bulk_mark_emails_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **bulk_mark_read_request** | [**BulkMarkReadRequest**](BulkMarkReadRequest.md)|  | 

### Return type

[**BulkMarkReadResponse**](BulkMarkReadResponse.md)

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

# **create_draft**
> DraftResponse create_draft(create_draft_request, x_workspace_id=x_workspace_id)

Create a draft.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_draft_request import CreateDraftRequest
from spatio.models.draft_response import DraftResponse
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
    api_instance = spatio.MailApi(api_client)
    create_draft_request = spatio.CreateDraftRequest() # CreateDraftRequest | 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a draft.
        api_response = api_instance.create_draft(create_draft_request, x_workspace_id=x_workspace_id)
        print("The response of MailApi->create_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->create_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_draft_request** | [**CreateDraftRequest**](CreateDraftRequest.md)|  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**DraftResponse**](DraftResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Draft created. |  -  |
**400** | Invalid body or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_email_label**
> CreateLabelResponse create_email_label(create_label_request, account_id=account_id, x_workspace_id=x_workspace_id)

Create a label.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_label_request import CreateLabelRequest
from spatio.models.create_label_response import CreateLabelResponse
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
    api_instance = spatio.MailApi(api_client)
    create_label_request = spatio.CreateLabelRequest() # CreateLabelRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a label.
        api_response = api_instance.create_email_label(create_label_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->create_email_label:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->create_email_label: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_label_request** | [**CreateLabelRequest**](CreateLabelRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**CreateLabelResponse**](CreateLabelResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Label created. |  -  |
**400** | Invalid body or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_mail_template**
> Dict[str, object] create_mail_template(request_body)

Create a mail template.

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
    api_instance = spatio.MailApi(api_client)
    request_body = None # Dict[str, object] | 

    try:
        # Create a mail template.
        api_response = api_instance.create_mail_template(request_body)
        print("The response of MailApi->create_mail_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->create_mail_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**201** | Created template. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_draft**
> delete_draft(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a draft.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Draft id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a draft.
        api_instance.delete_draft(id, account_id=account_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling MailApi->delete_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Draft id. | 
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
**204** | Draft deleted. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Draft not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_email**
> SuccessFlag delete_email(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete an email.

Soft-deletes (moves to provider trash).

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Email message id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete an email.
        api_response = api_instance.delete_email(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->delete_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->delete_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Email message id. | 
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
**404** | Message not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_email_label**
> delete_email_label(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a label.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Label id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a label.
        api_instance.delete_email_label(id, account_id=account_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling MailApi->delete_email_label: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Label id. | 
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
**204** | Label deleted. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Label not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_mail_template**
> delete_mail_template(id)

Delete a mail template.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete a mail template.
        api_instance.delete_mail_template(id)
    except Exception as e:
        print("Exception when calling MailApi->delete_mail_template: %s\n" % e)
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

# **get_email**
> GetEmailResponse get_email(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one email.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.get_email_response import GetEmailResponse
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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Email message id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one email.
        api_response = api_instance.get_email(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->get_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->get_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Email message id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**GetEmailResponse**](GetEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The email. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Message not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_attachment**
> bytes get_email_attachment(message_id, attachment_id, account_id=account_id, x_workspace_id=x_workspace_id)

Download an attachment.

Streams the attachment binary. Response `Content-Type` matches
the attachment's declared MIME type; `Content-Disposition` sets
the filename.


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
    api_instance = spatio.MailApi(api_client)
    message_id = 'message_id_example' # str | Message id the attachment belongs to.
    attachment_id = 'attachment_id_example' # str | Attachment id within the message.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Download an attachment.
        api_response = api_instance.get_email_attachment(message_id, attachment_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->get_email_attachment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->get_email_attachment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Message id the attachment belongs to. | 
 **attachment_id** | **str**| Attachment id within the message. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

**bytes**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/octet-stream, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The attachment binary. |  -  |
**400** | Missing ids or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Attachment not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_email_thread**
> GetThreadResponse get_email_thread(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch a thread (the conversation a message belongs to).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.get_thread_response import GetThreadResponse
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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Thread id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch a thread (the conversation a message belongs to).
        api_response = api_instance.get_email_thread(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->get_email_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->get_email_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Thread id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**GetThreadResponse**](GetThreadResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The thread. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Thread not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mail_template**
> Dict[str, object] get_mail_template(id)

Fetch a mail template.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch a mail template.
        api_response = api_instance.get_mail_template(id)
        print("The response of MailApi->get_mail_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->get_mail_template: %s\n" % e)
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
**200** | Template. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_mail_thread_tracking**
> Dict[str, object] get_mail_thread_tracking(thread_id)

Read mail-tracking events for a thread (open log, reply log, etc.).

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
    api_instance = spatio.MailApi(api_client)
    thread_id = 'thread_id_example' # str | 

    try:
        # Read mail-tracking events for a thread (open log, reply log, etc.).
        api_response = api_instance.get_mail_thread_tracking(thread_id)
        print("The response of MailApi->get_mail_thread_tracking:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->get_mail_thread_tracking: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **thread_id** | **str**|  | 

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
**200** | Tracking events. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **instantiate_mail_template**
> Dict[str, object] instantiate_mail_template(id, request_body)

Render a template with variables and return the resulting draft.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Render a template with variables and return the resulting draft.
        api_response = api_instance.instantiate_mail_template(id, request_body)
        print("The response of MailApi->instantiate_mail_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->instantiate_mail_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | Rendered draft. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_drafts**
> ListDraftsResponse list_drafts(x_workspace_id=x_workspace_id, account_ids=account_ids, providers=providers, limit=limit, next_page_token=next_page_token)

List drafts across connected mail accounts.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_drafts_response import ListDraftsResponse
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
    api_instance = spatio.MailApi(api_client)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    limit = 50 # int |  (optional) (default to 50)
    next_page_token = 'next_page_token_example' # str |  (optional)

    try:
        # List drafts across connected mail accounts.
        api_response = api_instance.list_drafts(x_workspace_id=x_workspace_id, account_ids=account_ids, providers=providers, limit=limit, next_page_token=next_page_token)
        print("The response of MailApi->list_drafts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->list_drafts: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **next_page_token** | **str**|  | [optional] 

### Return type

[**ListDraftsResponse**](ListDraftsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Draft list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_email_labels**
> ListLabelsResponse list_email_labels(account_id=account_id, x_workspace_id=x_workspace_id)

List labels on the resolved mail account.

Single-account list. The platform auto-resolves to the caller's
sole connected account; pass `?accountId=` to disambiguate when
multiple are connected.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_labels_response import ListLabelsResponse
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
    api_instance = spatio.MailApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # List labels on the resolved mail account.
        api_response = api_instance.list_email_labels(account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->list_email_labels:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->list_email_labels: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**ListLabelsResponse**](ListLabelsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Label list. |  -  |
**400** | Ambiguous account or no mail provider connected. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_emails**
> ListEmailsResponse list_emails(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, query=query, labels=labels, folder=folder, limit=limit, offset=offset)

List emails across connected mail accounts.

Fan-out list. Returns messages across every connected mail
provider unless filtered. Pass `?accountIds=` (repeatable) to
restrict to specific accounts, `?providers=` to restrict to
specific provider ids, or both for the intersection.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_emails_response import ListEmailsResponse
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
    api_instance = spatio.MailApi(api_client)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    query = 'query_example' # str | Provider-specific full-text query (e.g. Gmail search syntax). (optional)
    labels = ['labels_example'] # List[str] | Repeatable. Filter to messages carrying every label. (optional)
    folder = 'folder_example' # str | Logical folder filter. Canonical values: `inbox`, `sent`, `starred`, `trash`, `archive`. Provider-specific folders accepted as opaque strings.  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List emails across connected mail accounts.
        api_response = api_instance.list_emails(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, query=query, labels=labels, folder=folder, limit=limit, offset=offset)
        print("The response of MailApi->list_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->list_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **query** | **str**| Provider-specific full-text query (e.g. Gmail search syntax). | [optional] 
 **labels** | [**List[str]**](str.md)| Repeatable. Filter to messages carrying every label. | [optional] 
 **folder** | **str**| Logical folder filter. Canonical values: &#x60;inbox&#x60;, &#x60;sent&#x60;, &#x60;starred&#x60;, &#x60;trash&#x60;, &#x60;archive&#x60;. Provider-specific folders accepted as opaque strings.  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **offset** | **int**|  | [optional] [default to 0]

### Return type

[**ListEmailsResponse**](ListEmailsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Email list. |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Resolver or fan-out failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_mail_templates**
> Dict[str, object] list_mail_templates()

List the caller's saved mail templates.

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
    api_instance = spatio.MailApi(api_client)

    try:
        # List the caller's saved mail templates.
        api_response = api_instance.list_mail_templates()
        print("The response of MailApi->list_mail_templates:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->list_mail_templates: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

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
**200** | Template envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **reply_email**
> SendEmailResponse reply_email(message_id, reply_email_request, x_workspace_id=x_workspace_id)

Reply to a specific email.

The original message is identified by `?messageId=`. Body
defaults to the original sender as recipient — pass `to`,
`cc`, `bcc` to override.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.reply_email_request import ReplyEmailRequest
from spatio.models.send_email_response import SendEmailResponse
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
    api_instance = spatio.MailApi(api_client)
    message_id = 'message_id_example' # str | Id of the message being replied to.
    reply_email_request = spatio.ReplyEmailRequest() # ReplyEmailRequest | 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Reply to a specific email.
        api_response = api_instance.reply_email(message_id, reply_email_request, x_workspace_id=x_workspace_id)
        print("The response of MailApi->reply_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->reply_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Id of the message being replied to. | 
 **reply_email_request** | [**ReplyEmailRequest**](ReplyEmailRequest.md)|  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Send result. |  -  |
**400** | Missing messageId or invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Original message not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **save_mail_template**
> Dict[str, object] save_mail_template(request_body)

Save-or-create endpoint used by the renderer's \"save as template\" flow. Distinct from POST /v1/mail/templates which is the strict create. 

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
    api_instance = spatio.MailApi(api_client)
    request_body = None # Dict[str, object] | 

    try:
        # Save-or-create endpoint used by the renderer's \"save as template\" flow. Distinct from POST /v1/mail/templates which is the strict create. 
        api_response = api_instance.save_mail_template(request_body)
        print("The response of MailApi->save_mail_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->save_mail_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | Saved template. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_emails**
> SearchEmailsResponse search_emails(q, account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, var_from=var_from, to=to, subject=subject, has_attachment=has_attachment, is_unread=is_unread, is_starred=is_starred, labels=labels, after=after, before=before, limit=limit, next_page_token=next_page_token)

Structured search across connected mail accounts.

Fan-out search. Mirrors `listEmails`'s account/provider filter
semantics. Date range filters are inclusive. The query string
itself is passed via `?q=` (not `?query=`); structured filters
go in their own params.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.search_emails_response import SearchEmailsResponse
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
    api_instance = spatio.MailApi(api_client)
    q = 'q_example' # str | Provider-specific full-text query string.
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    var_from = 'var_from_example' # str |  (optional)
    to = 'to_example' # str |  (optional)
    subject = 'subject_example' # str |  (optional)
    has_attachment = True # bool |  (optional)
    is_unread = True # bool |  (optional)
    is_starred = True # bool |  (optional)
    labels = ['labels_example'] # List[str] |  (optional)
    after = '2013-10-20T19:20:30+01:00' # datetime | Inclusive lower-bound date. (optional)
    before = '2013-10-20T19:20:30+01:00' # datetime | Inclusive upper-bound date. (optional)
    limit = 50 # int |  (optional) (default to 50)
    next_page_token = 'next_page_token_example' # str | Cursor returned by the previous call. (optional)

    try:
        # Structured search across connected mail accounts.
        api_response = api_instance.search_emails(q, account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, var_from=var_from, to=to, subject=subject, has_attachment=has_attachment, is_unread=is_unread, is_starred=is_starred, labels=labels, after=after, before=before, limit=limit, next_page_token=next_page_token)
        print("The response of MailApi->search_emails:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->search_emails: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**| Provider-specific full-text query string. | 
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **var_from** | **str**|  | [optional] 
 **to** | **str**|  | [optional] 
 **subject** | **str**|  | [optional] 
 **has_attachment** | **bool**|  | [optional] 
 **is_unread** | **bool**|  | [optional] 
 **is_starred** | **bool**|  | [optional] 
 **labels** | [**List[str]**](str.md)|  | [optional] 
 **after** | **datetime**| Inclusive lower-bound date. | [optional] 
 **before** | **datetime**| Inclusive upper-bound date. | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **next_page_token** | **str**| Cursor returned by the previous call. | [optional] 

### Return type

[**SearchEmailsResponse**](SearchEmailsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results. |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Resolver or provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_draft**
> SendEmailResponse send_draft(id, account_id=account_id, x_workspace_id=x_workspace_id)

Send a draft.

Submits the draft as an outbound message. The draft is
consumed by the provider — subsequent `getDraft`/`updateDraft`
calls return `404`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.send_email_response import SendEmailResponse
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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Draft id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Send a draft.
        api_response = api_instance.send_draft(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->send_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->send_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Draft id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Send result. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Draft not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_email**
> SendEmailResponse send_email(send_email_request, x_workspace_id=x_workspace_id)

Send an email.

Sends through the resolved connected account (auto-picks if
the caller has exactly one connected mail account; errors
`ambiguous_account` otherwise unless `accountId` is supplied).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.send_email_request import SendEmailRequest
from spatio.models.send_email_response import SendEmailResponse
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
    api_instance = spatio.MailApi(api_client)
    send_email_request = spatio.SendEmailRequest() # SendEmailRequest | 
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Send an email.
        api_response = api_instance.send_email(send_email_request, x_workspace_id=x_workspace_id)
        print("The response of MailApi->send_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->send_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **send_email_request** | [**SendEmailRequest**](SendEmailRequest.md)|  | 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SendEmailResponse**](SendEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Send result. |  -  |
**400** | Invalid body, ambiguous account (&#x60;code: ambiguous_account&#x60;), or no mail provider connected (&#x60;code: no_mail_provider&#x60;).  |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_draft**
> DraftResponse update_draft(id, update_draft_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a draft (full replacement of provided fields).

PUT replaces the full set of provided fields on the draft.
Fields omitted from the body are not modified.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.draft_response import DraftResponse
from spatio.models.update_draft_request import UpdateDraftRequest
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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Draft id.
    update_draft_request = spatio.UpdateDraftRequest() # UpdateDraftRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a draft (full replacement of provided fields).
        api_response = api_instance.update_draft(id, update_draft_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->update_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->update_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Draft id. | 
 **update_draft_request** | [**UpdateDraftRequest**](UpdateDraftRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**DraftResponse**](DraftResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated draft. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Draft not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_email**
> UpdateEmailResponse update_email(id, update_email_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update an email (mark read/star, add/remove labels).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.update_email_request import UpdateEmailRequest
from spatio.models.update_email_response import UpdateEmailResponse
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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | Email message id.
    update_email_request = spatio.UpdateEmailRequest() # UpdateEmailRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update an email (mark read/star, add/remove labels).
        api_response = api_instance.update_email(id, update_email_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of MailApi->update_email:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->update_email: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Email message id. | 
 **update_email_request** | [**UpdateEmailRequest**](UpdateEmailRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**UpdateEmailResponse**](UpdateEmailResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated email. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Message not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_mail_template**
> Dict[str, object] update_mail_template(id, request_body)

Update a mail template.

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
    api_instance = spatio.MailApi(api_client)
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Update a mail template.
        api_response = api_instance.update_mail_template(id, request_body)
        print("The response of MailApi->update_mail_template:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->update_mail_template: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
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
**200** | Updated. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_add_mail_message_labels**
> Dict[str, object] workspace_add_mail_message_labels(org, workspace, message_id, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    message_id = 'message_id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_add_mail_message_labels(org, workspace, message_id, request_body)
        print("The response of MailApi->workspace_add_mail_message_labels:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_add_mail_message_labels: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **message_id** | **str**|  | 
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
**200** | Added |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_create_mail_draft**
> Dict[str, object] workspace_create_mail_draft(org, workspace, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_create_mail_draft(org, workspace, request_body)
        print("The response of MailApi->workspace_create_mail_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_create_mail_draft: %s\n" % e)
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

# **workspace_create_mail_label**
> Dict[str, object] workspace_create_mail_label(org, workspace, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_create_mail_label(org, workspace, request_body)
        print("The response of MailApi->workspace_create_mail_label:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_create_mail_label: %s\n" % e)
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

# **workspace_delete_mail**
> workspace_delete_mail(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_delete_mail(org, workspace, id)
    except Exception as e:
        print("Exception when calling MailApi->workspace_delete_mail: %s\n" % e)
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

# **workspace_delete_mail_draft**
> workspace_delete_mail_draft(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_delete_mail_draft(org, workspace, id)
    except Exception as e:
        print("Exception when calling MailApi->workspace_delete_mail_draft: %s\n" % e)
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

# **workspace_delete_mail_label**
> workspace_delete_mail_label(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_instance.workspace_delete_mail_label(org, workspace, id)
    except Exception as e:
        print("Exception when calling MailApi->workspace_delete_mail_label: %s\n" % e)
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

# **workspace_get_mail**
> Dict[str, object] workspace_get_mail(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_mail(org, workspace, id)
        print("The response of MailApi->workspace_get_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_get_mail: %s\n" % e)
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
**200** | Email |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |
**404** | Not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_mail_attachment**
> Dict[str, object] workspace_get_mail_attachment(org, workspace, message_id, attachment_id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    message_id = 'message_id_example' # str | 
    attachment_id = 'attachment_id_example' # str | 

    try:
        api_response = api_instance.workspace_get_mail_attachment(org, workspace, message_id, attachment_id)
        print("The response of MailApi->workspace_get_mail_attachment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_get_mail_attachment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **message_id** | **str**|  | 
 **attachment_id** | **str**|  | 

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
**200** | Attachment |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_mail_by_id**
> Dict[str, object] workspace_get_mail_by_id(org, workspace, id)

Workspace-scoped renderer-compat alias for mail/email/{id}.

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        # Workspace-scoped renderer-compat alias for mail/email/{id}.
        api_response = api_instance.workspace_get_mail_by_id(org, workspace, id)
        print("The response of MailApi->workspace_get_mail_by_id:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_get_mail_by_id: %s\n" % e)
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
**200** | Email |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_mail_draft**
> Dict[str, object] workspace_get_mail_draft(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_mail_draft(org, workspace, id)
        print("The response of MailApi->workspace_get_mail_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_get_mail_draft: %s\n" % e)
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
**200** | Draft |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_mail_thread**
> Dict[str, object] workspace_get_mail_thread(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_mail_thread(org, workspace, id)
        print("The response of MailApi->workspace_get_mail_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_get_mail_thread: %s\n" % e)
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
**200** | Thread |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_mail**
> Dict[str, object] workspace_list_mail(org, workspace)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_mail(org, workspace)
        print("The response of MailApi->workspace_list_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_list_mail: %s\n" % e)
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
**200** | Email list |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_mail_drafts**
> Dict[str, object] workspace_list_mail_drafts(org, workspace)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_mail_drafts(org, workspace)
        print("The response of MailApi->workspace_list_mail_drafts:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_list_mail_drafts: %s\n" % e)
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
**200** | Drafts |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_mail_labels**
> Dict[str, object] workspace_list_mail_labels(org, workspace)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_mail_labels(org, workspace)
        print("The response of MailApi->workspace_list_mail_labels:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_list_mail_labels: %s\n" % e)
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
**200** | Labels |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_patch_mail**
> Dict[str, object] workspace_patch_mail(org, workspace, id, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_patch_mail(org, workspace, id, request_body)
        print("The response of MailApi->workspace_patch_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_patch_mail: %s\n" % e)
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

# **workspace_remove_mail_message_label**
> workspace_remove_mail_message_label(org, workspace, message_id, label_id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    message_id = 'message_id_example' # str | 
    label_id = 'label_id_example' # str | 

    try:
        api_instance.workspace_remove_mail_message_label(org, workspace, message_id, label_id)
    except Exception as e:
        print("Exception when calling MailApi->workspace_remove_mail_message_label: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **message_id** | **str**|  | 
 **label_id** | **str**|  | 

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
**204** | Removed |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_reply_mail**
> Dict[str, object] workspace_reply_mail(org, workspace, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_reply_mail(org, workspace, request_body)
        print("The response of MailApi->workspace_reply_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_reply_mail: %s\n" % e)
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
**200** | Replied |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_search_mail**
> Dict[str, object] workspace_search_mail(org, workspace, q=q)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    q = 'q_example' # str |  (optional)

    try:
        api_response = api_instance.workspace_search_mail(org, workspace, q=q)
        print("The response of MailApi->workspace_search_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_search_mail: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **org** | **str**|  | 
 **workspace** | **str**|  | 
 **q** | **str**|  | [optional] 

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
**200** | Results |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_send_mail**
> Dict[str, object] workspace_send_mail(org, workspace, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_send_mail(org, workspace, request_body)
        print("The response of MailApi->workspace_send_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_send_mail: %s\n" % e)
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
**200** | Sent |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_send_mail_draft**
> Dict[str, object] workspace_send_mail_draft(org, workspace, id)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_send_mail_draft(org, workspace, id)
        print("The response of MailApi->workspace_send_mail_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_send_mail_draft: %s\n" % e)
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
**200** | Sent |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_send_mail_email_alias**
> Dict[str, object] workspace_send_mail_email_alias(org, workspace, request_body)

Renderer-compat alias for /mail/send.

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        # Renderer-compat alias for /mail/send.
        api_response = api_instance.workspace_send_mail_email_alias(org, workspace, request_body)
        print("The response of MailApi->workspace_send_mail_email_alias:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_send_mail_email_alias: %s\n" % e)
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
**200** | Sent |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_update_mail**
> Dict[str, object] workspace_update_mail(org, workspace, id, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_update_mail(org, workspace, id, request_body)
        print("The response of MailApi->workspace_update_mail:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_update_mail: %s\n" % e)
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

# **workspace_update_mail_draft**
> Dict[str, object] workspace_update_mail_draft(org, workspace, id, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_update_mail_draft(org, workspace, id, request_body)
        print("The response of MailApi->workspace_update_mail_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_update_mail_draft: %s\n" % e)
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

# **workspace_update_mail_label**
> Dict[str, object] workspace_update_mail_label(org, workspace, id, request_body)

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
    api_instance = spatio.MailApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_update_mail_label(org, workspace, id, request_body)
        print("The response of MailApi->workspace_update_mail_label:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling MailApi->workspace_update_mail_label: %s\n" % e)
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

