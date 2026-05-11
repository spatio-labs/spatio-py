# spatio.RealtimeApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**issue_collaboration_token**](RealtimeApi.md#issue_collaboration_token) | **POST** /v1/realtime/collaboration-token | Exchange a bearer token for a short-lived Yjs collaboration JWT.


# **issue_collaboration_token**
> IssueCollaborationToken200Response issue_collaboration_token(issue_collaboration_token_request=issue_collaboration_token_request)

Exchange a bearer token for a short-lived Yjs collaboration JWT.

The Yjs Cloudflare Worker that powers live document
collaboration (`wss://realtime-collaboration.<account>.workers.dev`)
only accepts platform-signed JWTs. Third-party clients holding
an OAuth access token or PAT call this endpoint to mint a
5-minute collaboration JWT they can present to the worker.

The minted JWT inherits user + workspace identity from the
presenting bearer token. Optionally scope it to a single room
by supplying `room` in the request body.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.issue_collaboration_token200_response import IssueCollaborationToken200Response
from spatio.models.issue_collaboration_token_request import IssueCollaborationTokenRequest
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
    api_instance = spatio.RealtimeApi(api_client)
    issue_collaboration_token_request = spatio.IssueCollaborationTokenRequest() # IssueCollaborationTokenRequest |  (optional)

    try:
        # Exchange a bearer token for a short-lived Yjs collaboration JWT.
        api_response = api_instance.issue_collaboration_token(issue_collaboration_token_request=issue_collaboration_token_request)
        print("The response of RealtimeApi->issue_collaboration_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling RealtimeApi->issue_collaboration_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **issue_collaboration_token_request** | [**IssueCollaborationTokenRequest**](IssueCollaborationTokenRequest.md)|  | [optional] 

### Return type

[**IssueCollaborationToken200Response**](IssueCollaborationToken200Response.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Token issued. |  -  |
**401** | Bearer token invalid. |  -  |
**500** | Server misconfigured (JWT_SECRET unset). |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

