# spatio.AgentsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_agent**](AgentsApi.md#create_agent) | **POST** /v1/agents | Create a new agent configuration.
[**create_agent_conversation**](AgentsApi.md#create_agent_conversation) | **POST** /v1/agent/conversations | Create a new agent-platform conversation.
[**create_agent_message**](AgentsApi.md#create_agent_message) | **POST** /v1/agent/conversations/{id}/messages | Append a message to an agent conversation.
[**delete_agent**](AgentsApi.md#delete_agent) | **DELETE** /v1/agents/{id} | Delete an agent configuration.
[**execute_agent_action**](AgentsApi.md#execute_agent_action) | **POST** /v1/agent/actions/execute | Execute an action through the agent platform.
[**get_agent**](AgentsApi.md#get_agent) | **GET** /v1/agents/{id} | Fetch one agent configuration.
[**get_agent_conversation**](AgentsApi.md#get_agent_conversation) | **GET** /v1/agent/conversations/{id} | Fetch one agent conversation.
[**get_agent_session_context**](AgentsApi.md#get_agent_session_context) | **GET** /v1/agent/session-context | Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn&#39;t fish on its first turn. 
[**list_agent_conversation_messages**](AgentsApi.md#list_agent_conversation_messages) | **GET** /v1/agent/conversations/{id}/messages | List messages on an agent conversation.
[**list_agent_conversations**](AgentsApi.md#list_agent_conversations) | **GET** /v1/agent/conversations | List the caller&#39;s agent-platform conversations. Distinct from &#x60;/v1/conversations&#x60; (renderer-driven sidebar persistence). 
[**list_agents**](AgentsApi.md#list_agents) | **GET** /v1/agents | List the caller&#39;s agent configurations.
[**list_preconfigured_agents**](AgentsApi.md#list_preconfigured_agents) | **GET** /v1/agents/preconfigured | Curated featured agents (e.g. \&quot;Claude Code\&quot;, \&quot;Research Assistant\&quot;). Read-only — these are surfaced by the renderer&#39;s preconfigured-picker UI. 
[**update_agent**](AgentsApi.md#update_agent) | **PATCH** /v1/agents/{id} | Update an agent configuration.


# **create_agent**
> Agent create_agent(create_agent_request)

Create a new agent configuration.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent import Agent
from spatio.models.create_agent_request import CreateAgentRequest
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
    api_instance = spatio.AgentsApi(api_client)
    create_agent_request = spatio.CreateAgentRequest() # CreateAgentRequest | 

    try:
        # Create a new agent configuration.
        api_response = api_instance.create_agent(create_agent_request)
        print("The response of AgentsApi->create_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->create_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_agent_request** | [**CreateAgentRequest**](CreateAgentRequest.md)|  | 

### Return type

[**Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created agent. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_agent_conversation**
> AgentConversation create_agent_conversation(create_agent_conversation_request=create_agent_conversation_request)

Create a new agent-platform conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_conversation import AgentConversation
from spatio.models.create_agent_conversation_request import CreateAgentConversationRequest
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
    api_instance = spatio.AgentsApi(api_client)
    create_agent_conversation_request = spatio.CreateAgentConversationRequest() # CreateAgentConversationRequest |  (optional)

    try:
        # Create a new agent-platform conversation.
        api_response = api_instance.create_agent_conversation(create_agent_conversation_request=create_agent_conversation_request)
        print("The response of AgentsApi->create_agent_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->create_agent_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_agent_conversation_request** | [**CreateAgentConversationRequest**](CreateAgentConversationRequest.md)|  | [optional] 

### Return type

[**AgentConversation**](AgentConversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created conversation. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_agent_message**
> AgentMessage create_agent_message(id, create_agent_message_request)

Append a message to an agent conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_message import AgentMessage
from spatio.models.create_agent_message_request import CreateAgentMessageRequest
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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 
    create_agent_message_request = spatio.CreateAgentMessageRequest() # CreateAgentMessageRequest | 

    try:
        # Append a message to an agent conversation.
        api_response = api_instance.create_agent_message(id, create_agent_message_request)
        print("The response of AgentsApi->create_agent_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->create_agent_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **create_agent_message_request** | [**CreateAgentMessageRequest**](CreateAgentMessageRequest.md)|  | 

### Return type

[**AgentMessage**](AgentMessage.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Created message. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_agent**
> delete_agent(id)

Delete an agent configuration.

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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete an agent configuration.
        api_instance.delete_agent(id)
    except Exception as e:
        print("Exception when calling AgentsApi->delete_agent: %s\n" % e)
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

# **execute_agent_action**
> ExecuteActionResponse execute_agent_action(execute_action_request)

Execute an action through the agent platform.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.execute_action_request import ExecuteActionRequest
from spatio.models.execute_action_response import ExecuteActionResponse
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
    api_instance = spatio.AgentsApi(api_client)
    execute_action_request = spatio.ExecuteActionRequest() # ExecuteActionRequest | 

    try:
        # Execute an action through the agent platform.
        api_response = api_instance.execute_agent_action(execute_action_request)
        print("The response of AgentsApi->execute_agent_action:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->execute_agent_action: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **execute_action_request** | [**ExecuteActionRequest**](ExecuteActionRequest.md)|  | 

### Return type

[**ExecuteActionResponse**](ExecuteActionResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Execution result. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent**
> Agent get_agent(id)

Fetch one agent configuration.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent import Agent
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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch one agent configuration.
        api_response = api_instance.get_agent(id)
        print("The response of AgentsApi->get_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->get_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Agent not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_conversation**
> AgentConversation get_agent_conversation(id)

Fetch one agent conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_conversation import AgentConversation
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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch one agent conversation.
        api_response = api_instance.get_agent_conversation(id)
        print("The response of AgentsApi->get_agent_conversation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->get_agent_conversation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**AgentConversation**](AgentConversation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Conversation. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_agent_session_context**
> AgentSessionContext get_agent_session_context()

Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn't fish on its first turn. 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_session_context import AgentSessionContext
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
    api_instance = spatio.AgentsApi(api_client)

    try:
        # Identity bundle for the SessionStart hook (user + org + workspace + connected accounts) so the agent doesn't fish on its first turn. 
        api_response = api_instance.get_agent_session_context()
        print("The response of AgentsApi->get_agent_session_context:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->get_agent_session_context: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AgentSessionContext**](AgentSessionContext.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session context. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agent_conversation_messages**
> AgentMessageListResponse list_agent_conversation_messages(id)

List messages on an agent conversation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_message_list_response import AgentMessageListResponse
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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 

    try:
        # List messages on an agent conversation.
        api_response = api_instance.list_agent_conversation_messages(id)
        print("The response of AgentsApi->list_agent_conversation_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agent_conversation_messages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**AgentMessageListResponse**](AgentMessageListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Message envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agent_conversations**
> AgentConversationListResponse list_agent_conversations()

List the caller's agent-platform conversations. Distinct from `/v1/conversations` (renderer-driven sidebar persistence). 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_conversation_list_response import AgentConversationListResponse
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
    api_instance = spatio.AgentsApi(api_client)

    try:
        # List the caller's agent-platform conversations. Distinct from `/v1/conversations` (renderer-driven sidebar persistence). 
        api_response = api_instance.list_agent_conversations()
        print("The response of AgentsApi->list_agent_conversations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agent_conversations: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AgentConversationListResponse**](AgentConversationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Conversation envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_agents**
> AgentListResponse list_agents()

List the caller's agent configurations.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent_list_response import AgentListResponse
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
    api_instance = spatio.AgentsApi(api_client)

    try:
        # List the caller's agent configurations.
        api_response = api_instance.list_agents()
        print("The response of AgentsApi->list_agents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_agents: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**AgentListResponse**](AgentListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent list envelope. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_preconfigured_agents**
> List[PreconfiguredAgent] list_preconfigured_agents()

Curated featured agents (e.g. \"Claude Code\", \"Research Assistant\"). Read-only — these are surfaced by the renderer's preconfigured-picker UI. 

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.preconfigured_agent import PreconfiguredAgent
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
    api_instance = spatio.AgentsApi(api_client)

    try:
        # Curated featured agents (e.g. \"Claude Code\", \"Research Assistant\"). Read-only — these are surfaced by the renderer's preconfigured-picker UI. 
        api_response = api_instance.list_preconfigured_agents()
        print("The response of AgentsApi->list_preconfigured_agents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->list_preconfigured_agents: %s\n" % e)
```



### Parameters

This endpoint does not need any parameter.

### Return type

[**List[PreconfiguredAgent]**](PreconfiguredAgent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Bare array of preconfigured agents. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_agent**
> Agent update_agent(id, update_agent_request)

Update an agent configuration.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.agent import Agent
from spatio.models.update_agent_request import UpdateAgentRequest
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
    api_instance = spatio.AgentsApi(api_client)
    id = 'id_example' # str | 
    update_agent_request = spatio.UpdateAgentRequest() # UpdateAgentRequest | 

    try:
        # Update an agent configuration.
        api_response = api_instance.update_agent(id, update_agent_request)
        print("The response of AgentsApi->update_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AgentsApi->update_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_agent_request** | [**UpdateAgentRequest**](UpdateAgentRequest.md)|  | 

### Return type

[**Agent**](Agent.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated agent. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

