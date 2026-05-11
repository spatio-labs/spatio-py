# spatio.DirectMessagesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**add_dm_reaction**](DirectMessagesApi.md#add_dm_reaction) | **POST** /v1/direct-messages/messages/{messageId}/reactions | React to a DM message.
[**attach_to_dm_message**](DirectMessagesApi.md#attach_to_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/attachments | Attach a file/image/etc. to an existing DM message.
[**execute_dm_action**](DirectMessagesApi.md#execute_dm_action) | **POST** /v1/direct-messages/execute | Dispatch a DM action by id.
[**forward_dm_message**](DirectMessagesApi.md#forward_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/forward | Forward a DM message to another DM or channel.
[**get_dm_user**](DirectMessagesApi.md#get_dm_user) | **GET** /v1/direct-messages/users/{id} | Fetch one chat user.
[**list_direct_conversations_enriched**](DirectMessagesApi.md#list_direct_conversations_enriched) | **GET** /v1/direct-messages/conversations | Enriched DM conversation list with unread + pin + draft state.
[**list_direct_message_conversations**](DirectMessagesApi.md#list_direct_message_conversations) | **GET** /v1/direct-messages | List 1:1 and group DM conversations.
[**list_direct_messages**](DirectMessagesApi.md#list_direct_messages) | **GET** /v1/direct-messages/messages | List messages in a DM conversation.
[**list_dm_actions**](DirectMessagesApi.md#list_dm_actions) | **GET** /v1/direct-messages/actions | Discover the action catalog for DirectMessages.
[**list_dm_pinned_messages**](DirectMessagesApi.md#list_dm_pinned_messages) | **GET** /v1/direct-messages/{dmId}/pinned | List pinned messages in a DM conversation.
[**list_dm_thread_replies**](DirectMessagesApi.md#list_dm_thread_replies) | **GET** /v1/direct-messages/{dmId}/messages/{messageId}/replies | List replies in a DM message thread.
[**list_dm_users**](DirectMessagesApi.md#list_dm_users) | **GET** /v1/direct-messages/users | List chat users (DM contacts) across connected accounts.
[**mark_dm_read**](DirectMessagesApi.md#mark_dm_read) | **POST** /v1/direct-messages/{dmId}/read | Mark a DM message read.
[**mute_dm**](DirectMessagesApi.md#mute_dm) | **POST** /v1/direct-messages/{dmId}/mute | Mute a DM conversation (until a time, or forever).
[**pin_dm_conversation**](DirectMessagesApi.md#pin_dm_conversation) | **POST** /v1/direct-messages/{dmId}/pin | Pin a DM conversation to the top of the sidebar.
[**pin_dm_message**](DirectMessagesApi.md#pin_dm_message) | **POST** /v1/direct-messages/messages/{messageId}/pin | Pin a DM message.
[**post_dm_thread_reply**](DirectMessagesApi.md#post_dm_thread_reply) | **POST** /v1/direct-messages/{dmId}/messages/{messageId}/replies | Reply in a DM message thread.
[**remove_dm_reaction**](DirectMessagesApi.md#remove_dm_reaction) | **DELETE** /v1/direct-messages/messages/{messageId}/reactions/{emoji} | Remove a DM message reaction.
[**search_direct_messages**](DirectMessagesApi.md#search_direct_messages) | **GET** /v1/direct-messages/search | Search across DM messages.
[**send_direct_message**](DirectMessagesApi.md#send_direct_message) | **POST** /v1/direct-messages/messages | Send a DM.
[**set_dm_draft**](DirectMessagesApi.md#set_dm_draft) | **PUT** /v1/direct-messages/{dmId}/draft | Save the unsent draft text for a DM.
[**unpin_dm_conversation**](DirectMessagesApi.md#unpin_dm_conversation) | **DELETE** /v1/direct-messages/{dmId}/pin | Unpin a DM conversation.
[**unpin_dm_message**](DirectMessagesApi.md#unpin_dm_message) | **DELETE** /v1/direct-messages/messages/{messageId}/pin | Unpin a DM message.
[**workspace_execute_dm_action**](DirectMessagesApi.md#workspace_execute_dm_action) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/execute | 
[**workspace_get_dm_user**](DirectMessagesApi.md#workspace_get_dm_user) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users/{id} | 
[**workspace_list_direct_messages**](DirectMessagesApi.md#workspace_list_direct_messages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages | 
[**workspace_list_dm_actions**](DirectMessagesApi.md#workspace_list_dm_actions) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/actions | 
[**workspace_list_dm_conversations**](DirectMessagesApi.md#workspace_list_dm_conversations) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/conversations | 
[**workspace_list_dm_messages**](DirectMessagesApi.md#workspace_list_dm_messages) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages | 
[**workspace_list_dm_users**](DirectMessagesApi.md#workspace_list_dm_users) | **GET** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/users | 
[**workspace_send_direct_message**](DirectMessagesApi.md#workspace_send_direct_message) | **POST** /v1/organizations/{org}/workspaces/{workspace}/direct-messages/messages | 


# **add_dm_reaction**
> DMReactionResponse add_dm_reaction(message_id, dm_reaction_request)

React to a DM message.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_reaction_request import DMReactionRequest
from spatio.models.dm_reaction_response import DMReactionResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    dm_reaction_request = spatio.DMReactionRequest() # DMReactionRequest | 

    try:
        # React to a DM message.
        api_response = api_instance.add_dm_reaction(message_id, dm_reaction_request)
        print("The response of DirectMessagesApi->add_dm_reaction:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->add_dm_reaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **dm_reaction_request** | [**DMReactionRequest**](DMReactionRequest.md)|  | 

### Return type

[**DMReactionResponse**](DMReactionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated reactions. |  -  |
**400** | Invalid body or missing emoji. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **attach_to_dm_message**
> DMMessageEnvelope attach_to_dm_message(message_id, dm_attach_request)

Attach a file/image/etc. to an existing DM message.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_attach_request import DMAttachRequest
from spatio.models.dm_message_envelope import DMMessageEnvelope
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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    dm_attach_request = spatio.DMAttachRequest() # DMAttachRequest | 

    try:
        # Attach a file/image/etc. to an existing DM message.
        api_response = api_instance.attach_to_dm_message(message_id, dm_attach_request)
        print("The response of DirectMessagesApi->attach_to_dm_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->attach_to_dm_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **dm_attach_request** | [**DMAttachRequest**](DMAttachRequest.md)|  | 

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated message envelope. |  -  |
**400** | Invalid body or missing fields. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **execute_dm_action**
> ExecuteChatActionResponse execute_dm_action(execute_chat_action_request)

Dispatch a DM action by id.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.execute_chat_action_request import ExecuteChatActionRequest
from spatio.models.execute_chat_action_response import ExecuteChatActionResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    execute_chat_action_request = spatio.ExecuteChatActionRequest() # ExecuteChatActionRequest | 

    try:
        # Dispatch a DM action by id.
        api_response = api_instance.execute_dm_action(execute_chat_action_request)
        print("The response of DirectMessagesApi->execute_dm_action:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->execute_dm_action: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **execute_chat_action_request** | [**ExecuteChatActionRequest**](ExecuteChatActionRequest.md)|  | 

### Return type

[**ExecuteChatActionResponse**](ExecuteChatActionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Action result. |  -  |
**400** | Invalid body or unknown action_id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **forward_dm_message**
> DMMessageEnvelope forward_dm_message(message_id, dm_forward_request)

Forward a DM message to another DM or channel.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_forward_request import DMForwardRequest
from spatio.models.dm_message_envelope import DMMessageEnvelope
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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    dm_forward_request = spatio.DMForwardRequest() # DMForwardRequest | 

    try:
        # Forward a DM message to another DM or channel.
        api_response = api_instance.forward_dm_message(message_id, dm_forward_request)
        print("The response of DirectMessagesApi->forward_dm_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->forward_dm_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **dm_forward_request** | [**DMForwardRequest**](DMForwardRequest.md)|  | 

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Forwarded message envelope. |  -  |
**400** | Invalid body or missing destination. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dm_user**
> GetChatUserResponse get_dm_user(id, account_id=account_id)

Fetch one chat user.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.get_chat_user_response import GetChatUserResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    id = 'id_example' # str | Chat-user id (provider-scoped).
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Fetch one chat user.
        api_response = api_instance.get_dm_user(id, account_id=account_id)
        print("The response of DirectMessagesApi->get_dm_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->get_dm_user: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Chat-user id (provider-scoped). | 
 **account_id** | **str**|  | [optional] 

### Return type

[**GetChatUserResponse**](GetChatUserResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The user. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | User not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_direct_conversations_enriched**
> Dict[str, object] list_direct_conversations_enriched(account_id=account_id, x_workspace_id=x_workspace_id)

Enriched DM conversation list with unread + pin + draft state.

Native fast-path. Returns conversations augmented with the
DM-feature state (unread counts, pinned/muted flags, saved
drafts) the renderer's DM UI consumes. The shape is
provider-specific and treated as opaque.


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
    api_instance = spatio.DirectMessagesApi(api_client)
    account_id = 'account_id_example' # str |  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Enriched DM conversation list with unread + pin + draft state.
        api_response = api_instance.list_direct_conversations_enriched(account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of DirectMessagesApi->list_direct_conversations_enriched:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_direct_conversations_enriched: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_id** | **str**|  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

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
**200** | Enriched conversation list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_direct_message_conversations**
> ListChannelsResponse list_direct_message_conversations(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor, include_archived=include_archived)

List 1:1 and group DM conversations.

Returns DM-type conversations only (`type: im | mpim`).
Channel-type conversations are surfaced via `/v1/channels`.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_channels_response import ListChannelsResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 56 # int |  (optional)
    cursor = 'cursor_example' # str |  (optional)
    include_archived = False # bool |  (optional) (default to False)

    try:
        # List 1:1 and group DM conversations.
        api_response = api_instance.list_direct_message_conversations(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor, include_archived=include_archived)
        print("The response of DirectMessagesApi->list_direct_message_conversations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_direct_message_conversations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **limit** | **int**|  | [optional] 
 **cursor** | **str**|  | [optional] 
 **include_archived** | **bool**|  | [optional] [default to False]

### Return type

[**ListChannelsResponse**](ListChannelsResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | DM conversation list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_direct_messages**
> ListMessagesResponse list_direct_messages(channel, account_id=account_id, account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor, oldest_first=oldest_first)

List messages in a DM conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_messages_response import ListMessagesResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    channel = 'channel_example' # str | DM conversation id.
    account_id = 'account_id_example' # str |  (optional)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 56 # int |  (optional)
    cursor = 'cursor_example' # str |  (optional)
    oldest_first = True # bool |  (optional)

    try:
        # List messages in a DM conversation.
        api_response = api_instance.list_direct_messages(channel, account_id=account_id, account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor, oldest_first=oldest_first)
        print("The response of DirectMessagesApi->list_direct_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_direct_messages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **channel** | **str**| DM conversation id. | 
 **account_id** | **str**|  | [optional] 
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **limit** | **int**|  | [optional] 
 **cursor** | **str**|  | [optional] 
 **oldest_first** | **bool**|  | [optional] 

### Return type

[**ListMessagesResponse**](ListMessagesResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Message list. |  -  |
**400** | Missing channel id. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_dm_actions**
> ChatActionsList list_dm_actions()

Discover the action catalog for DirectMessages.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.chat_actions_list import ChatActionsList
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
    api_instance = spatio.DirectMessagesApi(api_client)

    try:
        # Discover the action catalog for DirectMessages.
        api_response = api_instance.list_dm_actions()
        print("The response of DirectMessagesApi->list_dm_actions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_dm_actions: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**ChatActionsList**](ChatActionsList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Action catalog. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_dm_pinned_messages**
> DMPinnedList list_dm_pinned_messages(dm_id, account_id=account_id)

List pinned messages in a DM conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_pinned_list import DMPinnedList
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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    account_id = 'account_id_example' # str |  (optional)

    try:
        # List pinned messages in a DM conversation.
        api_response = api_instance.list_dm_pinned_messages(dm_id, account_id=account_id)
        print("The response of DirectMessagesApi->list_dm_pinned_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_dm_pinned_messages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **account_id** | **str**|  | [optional] 

### Return type

[**DMPinnedList**](DMPinnedList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Pinned-message list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_dm_thread_replies**
> Dict[str, object] list_dm_thread_replies(dm_id, message_id, account_id=account_id)

List replies in a DM message thread.

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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    message_id = 'message_id_example' # str | Chat-message id.
    account_id = 'account_id_example' # str |  (optional)

    try:
        # List replies in a DM message thread.
        api_response = api_instance.list_dm_thread_replies(dm_id, message_id, account_id=account_id)
        print("The response of DirectMessagesApi->list_dm_thread_replies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_dm_thread_replies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **message_id** | **str**| Chat-message id. | 
 **account_id** | **str**|  | [optional] 

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
**200** | Thread replies. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_dm_users**
> ListChatUsersResponse list_dm_users(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor)

List chat users (DM contacts) across connected accounts.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.list_chat_users_response import ListChatUsersResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    account_ids = ['account_ids_example'] # List[str] | Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to `providers` — when both are set the intersection is used.  (optional)
    providers = ['providers_example'] # List[str] | Repeatable. Restrict to these provider ids (`gmail`, `outlook`). (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 56 # int |  (optional)
    cursor = 'cursor_example' # str |  (optional)

    try:
        # List chat users (DM contacts) across connected accounts.
        api_response = api_instance.list_dm_users(account_ids=account_ids, providers=providers, x_workspace_id=x_workspace_id, limit=limit, cursor=cursor)
        print("The response of DirectMessagesApi->list_dm_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->list_dm_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **account_ids** | [**List[str]**](str.md)| Repeatable. Restrict to these connected-account row ids. Mutually orthogonal to &#x60;providers&#x60; — when both are set the intersection is used.  | [optional] 
 **providers** | [**List[str]**](str.md)| Repeatable. Restrict to these provider ids (&#x60;gmail&#x60;, &#x60;outlook&#x60;). | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **limit** | **int**|  | [optional] 
 **cursor** | **str**|  | [optional] 

### Return type

[**ListChatUsersResponse**](ListChatUsersResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | User list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mark_dm_read**
> SuccessFlag mark_dm_read(dm_id, dm_mark_read_request)

Mark a DM message read.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_mark_read_request import DMMarkReadRequest
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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    dm_mark_read_request = spatio.DMMarkReadRequest() # DMMarkReadRequest | 

    try:
        # Mark a DM message read.
        api_response = api_instance.mark_dm_read(dm_id, dm_mark_read_request)
        print("The response of DirectMessagesApi->mark_dm_read:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->mark_dm_read: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **dm_mark_read_request** | [**DMMarkReadRequest**](DMMarkReadRequest.md)|  | 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**400** | Missing body or messageId. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **mute_dm**
> DMMuteResponse mute_dm(dm_id, dm_mute_request)

Mute a DM conversation (until a time, or forever).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_mute_request import DMMuteRequest
from spatio.models.dm_mute_response import DMMuteResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    dm_mute_request = spatio.DMMuteRequest() # DMMuteRequest | 

    try:
        # Mute a DM conversation (until a time, or forever).
        api_response = api_instance.mute_dm(dm_id, dm_mute_request)
        print("The response of DirectMessagesApi->mute_dm:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->mute_dm: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **dm_mute_request** | [**DMMuteRequest**](DMMuteRequest.md)|  | 

### Return type

[**DMMuteResponse**](DMMuteResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Mute applied. |  -  |
**400** | Invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pin_dm_conversation**
> SuccessFlag pin_dm_conversation(dm_id, account_id=account_id)

Pin a DM conversation to the top of the sidebar.

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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Pin a DM conversation to the top of the sidebar.
        api_response = api_instance.pin_dm_conversation(dm_id, account_id=account_id)
        print("The response of DirectMessagesApi->pin_dm_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->pin_dm_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **account_id** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pin_dm_message**
> SuccessFlag pin_dm_message(message_id, channel_membership_request=channel_membership_request)

Pin a DM message.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.channel_membership_request import ChannelMembershipRequest
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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    channel_membership_request = spatio.ChannelMembershipRequest() # ChannelMembershipRequest |  (optional)

    try:
        # Pin a DM message.
        api_response = api_instance.pin_dm_message(message_id, channel_membership_request=channel_membership_request)
        print("The response of DirectMessagesApi->pin_dm_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->pin_dm_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **channel_membership_request** | [**ChannelMembershipRequest**](ChannelMembershipRequest.md)|  | [optional] 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_dm_thread_reply**
> DMMessageEnvelope post_dm_thread_reply(dm_id, message_id, dm_thread_reply_request, account_id=account_id)

Reply in a DM message thread.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_message_envelope import DMMessageEnvelope
from spatio.models.dm_thread_reply_request import DMThreadReplyRequest
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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    message_id = 'message_id_example' # str | Chat-message id.
    dm_thread_reply_request = spatio.DMThreadReplyRequest() # DMThreadReplyRequest | 
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Reply in a DM message thread.
        api_response = api_instance.post_dm_thread_reply(dm_id, message_id, dm_thread_reply_request, account_id=account_id)
        print("The response of DirectMessagesApi->post_dm_thread_reply:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->post_dm_thread_reply: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **message_id** | **str**| Chat-message id. | 
 **dm_thread_reply_request** | [**DMThreadReplyRequest**](DMThreadReplyRequest.md)|  | 
 **account_id** | **str**|  | [optional] 

### Return type

[**DMMessageEnvelope**](DMMessageEnvelope.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Reply created. |  -  |
**400** | Invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **remove_dm_reaction**
> DMReactionResponse remove_dm_reaction(message_id, emoji, account_id=account_id)

Remove a DM message reaction.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_reaction_response import DMReactionResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    emoji = 'emoji_example' # str | Reaction emoji (e.g. `+1`, `eyes`, `pepper`).
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Remove a DM message reaction.
        api_response = api_instance.remove_dm_reaction(message_id, emoji, account_id=account_id)
        print("The response of DirectMessagesApi->remove_dm_reaction:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->remove_dm_reaction: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **emoji** | **str**| Reaction emoji (e.g. &#x60;+1&#x60;, &#x60;eyes&#x60;, &#x60;pepper&#x60;). | 
 **account_id** | **str**|  | [optional] 

### Return type

[**DMReactionResponse**](DMReactionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated reactions. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_direct_messages**
> DMSearchResults search_direct_messages(q, limit=limit, dm_id=dm_id, user=user, account_id=account_id)

Search across DM messages.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_search_results import DMSearchResults
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
    api_instance = spatio.DirectMessagesApi(api_client)
    q = 'q_example' # str | Free-form query string.
    limit = 56 # int |  (optional)
    dm_id = 'dm_id_example' # str | Restrict to one conversation. (optional)
    user = 'user_example' # str | Restrict to messages from this user id. (optional)
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Search across DM messages.
        api_response = api_instance.search_direct_messages(q, limit=limit, dm_id=dm_id, user=user, account_id=account_id)
        print("The response of DirectMessagesApi->search_direct_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->search_direct_messages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **q** | **str**| Free-form query string. | 
 **limit** | **int**|  | [optional] 
 **dm_id** | **str**| Restrict to one conversation. | [optional] 
 **user** | **str**| Restrict to messages from this user id. | [optional] 
 **account_id** | **str**|  | [optional] 

### Return type

[**DMSearchResults**](DMSearchResults.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results (provider-shaped). |  -  |
**400** | Missing query. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **send_direct_message**
> SendChatMessageResponse send_direct_message(send_chat_message_request)

Send a DM.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.send_chat_message_request import SendChatMessageRequest
from spatio.models.send_chat_message_response import SendChatMessageResponse
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
    api_instance = spatio.DirectMessagesApi(api_client)
    send_chat_message_request = spatio.SendChatMessageRequest() # SendChatMessageRequest | 

    try:
        # Send a DM.
        api_response = api_instance.send_direct_message(send_chat_message_request)
        print("The response of DirectMessagesApi->send_direct_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->send_direct_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **send_chat_message_request** | [**SendChatMessageRequest**](SendChatMessageRequest.md)|  | 

### Return type

[**SendChatMessageResponse**](SendChatMessageResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Send result. |  -  |
**400** | Invalid body or missing channel. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_dm_draft**
> SuccessFlag set_dm_draft(dm_id, dm_set_draft_request)

Save the unsent draft text for a DM.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.dm_set_draft_request import DMSetDraftRequest
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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    dm_set_draft_request = spatio.DMSetDraftRequest() # DMSetDraftRequest | 

    try:
        # Save the unsent draft text for a DM.
        api_response = api_instance.set_dm_draft(dm_id, dm_set_draft_request)
        print("The response of DirectMessagesApi->set_dm_draft:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->set_dm_draft: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **dm_set_draft_request** | [**DMSetDraftRequest**](DMSetDraftRequest.md)|  | 

### Return type

[**SuccessFlag**](SuccessFlag.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Success ack. |  -  |
**400** | Invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unpin_dm_conversation**
> SuccessFlag unpin_dm_conversation(dm_id, account_id=account_id)

Unpin a DM conversation.

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
    api_instance = spatio.DirectMessagesApi(api_client)
    dm_id = 'dm_id_example' # str | Direct-message conversation id.
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Unpin a DM conversation.
        api_response = api_instance.unpin_dm_conversation(dm_id, account_id=account_id)
        print("The response of DirectMessagesApi->unpin_dm_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->unpin_dm_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **dm_id** | **str**| Direct-message conversation id. | 
 **account_id** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **unpin_dm_message**
> SuccessFlag unpin_dm_message(message_id, account_id=account_id)

Unpin a DM message.

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
    api_instance = spatio.DirectMessagesApi(api_client)
    message_id = 'message_id_example' # str | Chat-message id.
    account_id = 'account_id_example' # str |  (optional)

    try:
        # Unpin a DM message.
        api_response = api_instance.unpin_dm_message(message_id, account_id=account_id)
        print("The response of DirectMessagesApi->unpin_dm_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->unpin_dm_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **message_id** | **str**| Chat-message id. | 
 **account_id** | **str**|  | [optional] 

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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_execute_dm_action**
> Dict[str, object] workspace_execute_dm_action(org, workspace, request_body)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_execute_dm_action(org, workspace, request_body)
        print("The response of DirectMessagesApi->workspace_execute_dm_action:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_execute_dm_action: %s\n" % e)
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
**200** | Result |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_get_dm_user**
> Dict[str, object] workspace_get_dm_user(org, workspace, id)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    id = 'id_example' # str | 

    try:
        api_response = api_instance.workspace_get_dm_user(org, workspace, id)
        print("The response of DirectMessagesApi->workspace_get_dm_user:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_get_dm_user: %s\n" % e)
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
**200** | User |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_direct_messages**
> Dict[str, object] workspace_list_direct_messages(org, workspace)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_direct_messages(org, workspace)
        print("The response of DirectMessagesApi->workspace_list_direct_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_list_direct_messages: %s\n" % e)
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
**200** | DMs |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_dm_actions**
> Dict[str, object] workspace_list_dm_actions(org, workspace)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_dm_actions(org, workspace)
        print("The response of DirectMessagesApi->workspace_list_dm_actions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_list_dm_actions: %s\n" % e)
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
**200** | Actions |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_dm_conversations**
> Dict[str, object] workspace_list_dm_conversations(org, workspace)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_dm_conversations(org, workspace)
        print("The response of DirectMessagesApi->workspace_list_dm_conversations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_list_dm_conversations: %s\n" % e)
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
**200** | Conversations |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_dm_messages**
> Dict[str, object] workspace_list_dm_messages(org, workspace)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_dm_messages(org, workspace)
        print("The response of DirectMessagesApi->workspace_list_dm_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_list_dm_messages: %s\n" % e)
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
**200** | Messages |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_list_dm_users**
> Dict[str, object] workspace_list_dm_users(org, workspace)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 

    try:
        api_response = api_instance.workspace_list_dm_users(org, workspace)
        print("The response of DirectMessagesApi->workspace_list_dm_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_list_dm_users: %s\n" % e)
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
**200** | Users |  -  |
**401** | Unauthenticated |  -  |
**403** | Insufficient permission |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **workspace_send_direct_message**
> Dict[str, object] workspace_send_direct_message(org, workspace, request_body)

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
    api_instance = spatio.DirectMessagesApi(api_client)
    org = 'org_example' # str | 
    workspace = 'workspace_example' # str | 
    request_body = None # Dict[str, object] | 

    try:
        api_response = api_instance.workspace_send_direct_message(org, workspace, request_body)
        print("The response of DirectMessagesApi->workspace_send_direct_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DirectMessagesApi->workspace_send_direct_message: %s\n" % e)
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

