# spatio.SearchApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**federated_search**](SearchApi.md#federated_search) | **POST** /v1/search | Cross-platform federated search.


# **federated_search**
> FederatedSearch200Response federated_search(federated_search_request)

Cross-platform federated search.

Fans out to every platform's per-platform search method in
parallel, merges + dedupes results, and returns them in a
relevance-then-recency ranking with per-platform cursors for
pagination.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.federated_search200_response import FederatedSearch200Response
from spatio.models.federated_search_request import FederatedSearchRequest
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
    api_instance = spatio.SearchApi(api_client)
    federated_search_request = spatio.FederatedSearchRequest() # FederatedSearchRequest | 

    try:
        # Cross-platform federated search.
        api_response = api_instance.federated_search(federated_search_request)
        print("The response of SearchApi->federated_search:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SearchApi->federated_search: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **federated_search_request** | [**FederatedSearchRequest**](FederatedSearchRequest.md)|  | 

### Return type

[**FederatedSearch200Response**](FederatedSearch200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Search results. |  -  |
**400** | Missing query. |  -  |
**401** | Unauthorized. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

