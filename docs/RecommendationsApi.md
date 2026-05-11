# spatio.RecommendationsApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_recommendation**](RecommendationsApi.md#delete_recommendation) | **DELETE** /v1/recommendations/{id} | Delete a recommendation (hard delete; status-update is preferred).
[**get_recommendation**](RecommendationsApi.md#get_recommendation) | **GET** /v1/recommendations/{id} | Fetch one recommendation.
[**list_recommendations**](RecommendationsApi.md#list_recommendations) | **GET** /v1/recommendations | List recommendations for a workspace.
[**propose_recommendation**](RecommendationsApi.md#propose_recommendation) | **POST** /v1/recommendations | Agent-side propose endpoint (the &#x60;spatio_recommendations propose&#x60; MCP tool calls this).
[**update_recommendation_status**](RecommendationsApi.md#update_recommendation_status) | **PATCH** /v1/recommendations/{id}/status | Accept or dismiss a recommendation.


# **delete_recommendation**
> delete_recommendation(id)

Delete a recommendation (hard delete; status-update is preferred).

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
    api_instance = spatio.RecommendationsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Delete a recommendation (hard delete; status-update is preferred).
        api_instance.delete_recommendation(id)
    except Exception as e:
        print("Exception when calling RecommendationsApi->delete_recommendation: %s\n" % e)
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

# **get_recommendation**
> Recommendation get_recommendation(id)

Fetch one recommendation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.recommendation import Recommendation
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
    api_instance = spatio.RecommendationsApi(api_client)
    id = 'id_example' # str | 

    try:
        # Fetch one recommendation.
        api_response = api_instance.get_recommendation(id)
        print("The response of RecommendationsApi->get_recommendation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->get_recommendation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 

### Return type

[**Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recommendation. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_recommendations**
> RecommendationListResponse list_recommendations(workspace_id=workspace_id, status=status, limit=limit)

List recommendations for a workspace.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.recommendation_list_response import RecommendationListResponse
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
    api_instance = spatio.RecommendationsApi(api_client)
    workspace_id = 'workspace_id_example' # str |  (optional)
    status = 'status_example' # str |  (optional)
    limit = 56 # int |  (optional)

    try:
        # List recommendations for a workspace.
        api_response = api_instance.list_recommendations(workspace_id=workspace_id, status=status, limit=limit)
        print("The response of RecommendationsApi->list_recommendations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->list_recommendations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **workspace_id** | **str**|  | [optional] 
 **status** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] 

### Return type

[**RecommendationListResponse**](RecommendationListResponse.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Recommendation list. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **propose_recommendation**
> Recommendation propose_recommendation(propose_recommendation_request)

Agent-side propose endpoint (the `spatio_recommendations propose` MCP tool calls this).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.propose_recommendation_request import ProposeRecommendationRequest
from spatio.models.recommendation import Recommendation
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
    api_instance = spatio.RecommendationsApi(api_client)
    propose_recommendation_request = spatio.ProposeRecommendationRequest() # ProposeRecommendationRequest | 

    try:
        # Agent-side propose endpoint (the `spatio_recommendations propose` MCP tool calls this).
        api_response = api_instance.propose_recommendation(propose_recommendation_request)
        print("The response of RecommendationsApi->propose_recommendation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->propose_recommendation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **propose_recommendation_request** | [**ProposeRecommendationRequest**](ProposeRecommendationRequest.md)|  | 

### Return type

[**Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Proposed recommendation. |  -  |
**401** | Caller is not authenticated. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_recommendation_status**
> Recommendation update_recommendation_status(id, update_recommendation_status_request)

Accept or dismiss a recommendation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.recommendation import Recommendation
from spatio.models.update_recommendation_status_request import UpdateRecommendationStatusRequest
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
    api_instance = spatio.RecommendationsApi(api_client)
    id = 'id_example' # str | 
    update_recommendation_status_request = spatio.UpdateRecommendationStatusRequest() # UpdateRecommendationStatusRequest | 

    try:
        # Accept or dismiss a recommendation.
        api_response = api_instance.update_recommendation_status(id, update_recommendation_status_request)
        print("The response of RecommendationsApi->update_recommendation_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RecommendationsApi->update_recommendation_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**|  | 
 **update_recommendation_status_request** | [**UpdateRecommendationStatusRequest**](UpdateRecommendationStatusRequest.md)|  | 

### Return type

[**Recommendation**](Recommendation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated recommendation. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

