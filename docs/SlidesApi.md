# spatio.SlidesApi

All URIs are relative to *https://api.spatio.app*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_presentation**](SlidesApi.md#create_presentation) | **POST** /v1/slides | Create a presentation.
[**create_slide**](SlidesApi.md#create_slide) | **POST** /v1/slides/{id}/slides | Insert a slide.
[**create_slide_element**](SlidesApi.md#create_slide_element) | **POST** /v1/slides/{id}/slides/{slideId}/elements | Add a canvas element (text/shape/image) to a slide.
[**delete_presentation**](SlidesApi.md#delete_presentation) | **DELETE** /v1/slides/{id} | Delete a presentation.
[**delete_slide**](SlidesApi.md#delete_slide) | **DELETE** /v1/slides/{id}/slides/{slideId} | Delete a slide.
[**delete_slide_element**](SlidesApi.md#delete_slide_element) | **DELETE** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Delete a slide element.
[**disable_presentation_share**](SlidesApi.md#disable_presentation_share) | **DELETE** /v1/slides/{id}/share | Disable public sharing.
[**enable_presentation_share**](SlidesApi.md#enable_presentation_share) | **POST** /v1/slides/{id}/share | Enable (or update password on) public sharing.
[**export_presentation_pdf**](SlidesApi.md#export_presentation_pdf) | **POST** /v1/slides/{id}/export/pdf | Render the presentation as a PDF.
[**export_presentation_pptx**](SlidesApi.md#export_presentation_pptx) | **POST** /v1/slides/{id}/export/pptx | Render the presentation as a PowerPoint (.pptx) file.
[**get_presentation**](SlidesApi.md#get_presentation) | **GET** /v1/slides/{id} | Fetch one presentation.
[**get_presentation_share_settings**](SlidesApi.md#get_presentation_share_settings) | **GET** /v1/slides/{id}/share | Fetch share settings for a presentation.
[**get_public_presentation**](SlidesApi.md#get_public_presentation) | **GET** /public/slides/{token} | Fetch a publicly shared presentation.
[**get_slide**](SlidesApi.md#get_slide) | **GET** /v1/slides/{id}/slides/{slideId} | Fetch one slide.
[**get_slide_element**](SlidesApi.md#get_slide_element) | **GET** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Fetch one slide element.
[**list_presentations**](SlidesApi.md#list_presentations) | **GET** /v1/slides | List presentations across connected accounts.
[**list_slide_elements**](SlidesApi.md#list_slide_elements) | **GET** /v1/slides/{id}/slides/{slideId}/elements | List the canvas elements on a slide.
[**list_slides_in_presentation**](SlidesApi.md#list_slides_in_presentation) | **GET** /v1/slides/{id}/slides | List slides in a presentation.
[**rotate_presentation_share_token**](SlidesApi.md#rotate_presentation_share_token) | **POST** /v1/slides/{id}/share/rotate | Rotate the share token, invalidating outstanding URLs.
[**update_presentation**](SlidesApi.md#update_presentation) | **PATCH** /v1/slides/{id} | Update presentation metadata (partial).
[**update_slide**](SlidesApi.md#update_slide) | **PATCH** /v1/slides/{id}/slides/{slideId} | Update a slide (partial).
[**update_slide_element**](SlidesApi.md#update_slide_element) | **PATCH** /v1/slides/{id}/slides/{slideId}/elements/{elementId} | Update a slide element (partial).


# **create_presentation**
> Presentation create_presentation(create_presentation_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)

Create a presentation.

Creates a new deck under the target account. Target resolution
mirrors `POST /v1/notes` and `/v1/sheets`: body `accountId` →
`?accountId=` → body `provider` → `?provider=` → caller's
single connected account (errors with `ambiguous_account`
otherwise). The new deck is auto-seeded with one blank slide
so the renderer has something to display immediately.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_presentation_request import CreatePresentationRequest
from spatio.models.presentation import Presentation
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
    api_instance = spatio.SlidesApi(api_client)
    create_presentation_request = spatio.CreatePresentationRequest() # CreatePresentationRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Create a presentation.
        api_response = api_instance.create_presentation(create_presentation_request, account_id=account_id, provider=provider, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->create_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->create_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **create_presentation_request** | [**CreatePresentationRequest**](CreatePresentationRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **provider** | **str**| Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;). Selects every connected account for the provider. Mutually exclusive with &#x60;accountId&#x60;.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Presentation created. |  -  |
**400** | Invalid body, ambiguous account (&#x60;code: ambiguous_account&#x60;), or no slides provider connected (&#x60;code: no_slides_provider&#x60;).  |  -  |
**401** | Caller is not authenticated. |  -  |
**500** | Provider failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_slide**
> Slide create_slide(id, create_slide_request, account_id=account_id, x_workspace_id=x_workspace_id)

Insert a slide.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_slide_request import CreateSlideRequest
from spatio.models.slide import Slide
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    create_slide_request = spatio.CreateSlideRequest() # CreateSlideRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Insert a slide.
        api_response = api_instance.create_slide(id, create_slide_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->create_slide:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->create_slide: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **create_slide_request** | [**CreateSlideRequest**](CreateSlideRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Slide created. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_slide_element**
> SlideElement create_slide_element(id, slide_id, create_slide_element_request, account_id=account_id, x_workspace_id=x_workspace_id)

Add a canvas element (text/shape/image) to a slide.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.create_slide_element_request import CreateSlideElementRequest
from spatio.models.slide_element import SlideElement
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    create_slide_element_request = spatio.CreateSlideElementRequest() # CreateSlideElementRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Add a canvas element (text/shape/image) to a slide.
        api_response = api_instance.create_slide_element(id, slide_id, create_slide_element_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->create_slide_element:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->create_slide_element: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **create_slide_element_request** | [**CreateSlideElementRequest**](CreateSlideElementRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Element created. |  -  |
**400** | Invalid body, missing elementType, or missing path id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Slide not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_presentation**
> SuccessFlag delete_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a presentation.

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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a presentation.
        api_response = api_instance.delete_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->delete_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->delete_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
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
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_slide**
> SuccessFlag delete_slide(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a slide.

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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a slide.
        api_response = api_instance.delete_slide(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->delete_slide:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->delete_slide: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
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
**404** | Slide not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_slide_element**
> SuccessFlag delete_slide_element(id, slide_id, element_id, account_id=account_id, x_workspace_id=x_workspace_id)

Delete a slide element.

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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    element_id = 'element_id_example' # str | Slide-element id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Delete a slide element.
        api_response = api_instance.delete_slide_element(id, slide_id, element_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->delete_slide_element:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->delete_slide_element: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **element_id** | **str**| Slide-element id. | 
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
**404** | Element not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disable_presentation_share**
> disable_presentation_share(id, account_id=account_id, x_workspace_id=x_workspace_id)

Disable public sharing.

Owner-only. Subsequent public viewer requests 404.

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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Disable public sharing.
        api_instance.disable_presentation_share(id, account_id=account_id, x_workspace_id=x_workspace_id)
    except Exception as e:
        print("Exception when calling SlidesApi->disable_presentation_share: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
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
**204** | Sharing disabled. |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is not the deck owner. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_presentation_share**
> ShareSettings enable_presentation_share(id, account_id=account_id, x_workspace_id=x_workspace_id, enable_share_request=enable_share_request)

Enable (or update password on) public sharing.

Owner-only. With `setPassword: false` (or empty body), flips
the deck public without changing the password. With
`setPassword: true`, applies `password` (empty clears).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.enable_share_request import EnableShareRequest
from spatio.models.share_settings import ShareSettings
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    enable_share_request = spatio.EnableShareRequest() # EnableShareRequest |  (optional)

    try:
        # Enable (or update password on) public sharing.
        api_response = api_instance.enable_presentation_share(id, account_id=account_id, x_workspace_id=x_workspace_id, enable_share_request=enable_share_request)
        print("The response of SlidesApi->enable_presentation_share:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->enable_presentation_share: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **enable_share_request** | [**EnableShareRequest**](EnableShareRequest.md)|  | [optional] 

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated share settings. |  -  |
**400** | Password failed strength check. |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is not the deck owner. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_presentation_pdf**
> bytes export_presentation_pdf(id, account_id=account_id, x_workspace_id=x_workspace_id, storage=storage, filename=filename, export_pdf_request=export_pdf_request)

Render the presentation as a PDF.

Proxies to the Spatio export sidecar (Playwright). Two response
modes selected via `?storage=`:

  - `stream` (default) — response body is the PDF binary
    (`application/pdf`).
  - `r2` — uploads the rendered PDF to R2 storage and returns
    a JSON envelope with a 24-hour signed URL.

Returns `503 Service Unavailable` when the export sidecar is
not configured (dev fallback to the client-side exporter).


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.export_pdf_request import ExportPDFRequest
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    storage = stream # str |  (optional) (default to stream)
    filename = 'filename_example' # str | Sanitized base name for the downloaded PDF. (optional)
    export_pdf_request = spatio.ExportPDFRequest() # ExportPDFRequest |  (optional)

    try:
        # Render the presentation as a PDF.
        api_response = api_instance.export_presentation_pdf(id, account_id=account_id, x_workspace_id=x_workspace_id, storage=storage, filename=filename, export_pdf_request=export_pdf_request)
        print("The response of SlidesApi->export_presentation_pdf:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->export_presentation_pdf: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **storage** | **str**|  | [optional] [default to stream]
 **filename** | **str**| Sanitized base name for the downloaded PDF. | [optional] 
 **export_pdf_request** | [**ExportPDFRequest**](ExportPDFRequest.md)|  | [optional] 

### Return type

**bytes**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/pdf, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Either the PDF binary (when &#x60;?storage&#x3D;stream&#x60;) or a JSON envelope with a signed URL (when &#x60;?storage&#x3D;r2&#x60;).  |  -  |
**400** | Missing id, presentation has no slides, or invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |
**502** | Export sidecar unreachable or upstream R2 failure. |  -  |
**503** | Export sidecar not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **export_presentation_pptx**
> bytes export_presentation_pptx(id, account_id=account_id, x_workspace_id=x_workspace_id, storage=storage, filename=filename, export_pdf_request=export_pdf_request)

Render the presentation as a PowerPoint (.pptx) file.

Proxies to the Spatio export sidecar (Playwright + pptxgenjs).
Each slide is screenshotted at 2× device-pixel ratio and wrapped
into a PowerPoint .pptx as a full-bleed image. Visual fidelity is
preserved exactly — what renders in Spatio renders identically in
PowerPoint, Keynote, Google Slides — at the cost of in-PowerPoint
editability of slide content. Users edit slide content back in
Spatio (the source of truth), not inside PowerPoint.

Two response modes selected via `?storage=`:

  - `stream` (default) — response body is the PPTX binary
    (`application/vnd.openxmlformats-officedocument.presentationml.presentation`).
  - `r2` — uploads the rendered PPTX to R2 storage and returns
    a JSON envelope with a 24-hour signed URL.

Returns `503 Service Unavailable` when the export sidecar is
not configured.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.export_pdf_request import ExportPDFRequest
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    storage = stream # str |  (optional) (default to stream)
    filename = 'filename_example' # str | Sanitized base name for the downloaded PPTX. (optional)
    export_pdf_request = spatio.ExportPDFRequest() # ExportPDFRequest |  (optional)

    try:
        # Render the presentation as a PowerPoint (.pptx) file.
        api_response = api_instance.export_presentation_pptx(id, account_id=account_id, x_workspace_id=x_workspace_id, storage=storage, filename=filename, export_pdf_request=export_pdf_request)
        print("The response of SlidesApi->export_presentation_pptx:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->export_presentation_pptx: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 
 **storage** | **str**|  | [optional] [default to stream]
 **filename** | **str**| Sanitized base name for the downloaded PPTX. | [optional] 
 **export_pdf_request** | [**ExportPDFRequest**](ExportPDFRequest.md)|  | [optional] 

### Return type

**bytes**

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/vnd.openxmlformats-officedocument.presentationml.presentation, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Either the PPTX binary (when &#x60;?storage&#x3D;stream&#x60;) or a JSON envelope with a signed URL (when &#x60;?storage&#x3D;r2&#x60;).  |  -  |
**400** | Missing id, presentation has no slides, or invalid body. |  -  |
**401** | Caller is not authenticated. |  -  |
**502** | Export sidecar unreachable or upstream R2 failure. |  -  |
**503** | Export sidecar not configured. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_presentation**
> Presentation get_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one presentation.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.presentation import Presentation
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one presentation.
        api_response = api_instance.get_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->get_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->get_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The presentation. |  -  |
**400** | Missing id or ambiguous account. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_presentation_share_settings**
> ShareSettings get_presentation_share_settings(id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch share settings for a presentation.

Owner-only. Mirror of `GET /v1/notes/{id}/share` — same shape,
same fields. Returns the current public-share configuration,
including the share token and computed public viewer URL when
the deck is currently public.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.share_settings import ShareSettings
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch share settings for a presentation.
        api_response = api_instance.get_presentation_share_settings(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->get_presentation_share_settings:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->get_presentation_share_settings: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Current share settings. |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is not the deck owner. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_public_presentation**
> Dict[str, object] get_public_presentation(token, password=password)

Fetch a publicly shared presentation.

Unauthenticated. Mirror of `GET /public/notes/{token}`. The
share token is the credential. For password-protected decks
the password is supplied via `?password=`; the response
distinguishes "no password supplied" from "wrong password" so
the viewer can render the right prompt. Unknown tokens and
disabled-share decks both return `404` to prevent enumeration.


### Example


```python
import spatio
from spatio.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://api.spatio.app
# See configuration.py for a list of all supported configuration parameters.
configuration = spatio.Configuration(
    host = "https://api.spatio.app"
)


# Enter a context with an instance of the API client
with spatio.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = spatio.SlidesApi(api_client)
    token = 'token_example' # str | Opaque public-share token.
    password = 'password_example' # str | Optional viewer password. (optional)

    try:
        # Fetch a publicly shared presentation.
        api_response = api_instance.get_public_presentation(token, password=password)
        print("The response of SlidesApi->get_public_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->get_public_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **token** | **str**| Opaque public-share token. | 
 **password** | **str**| Optional viewer password. | [optional] 

### Return type

**Dict[str, object]**

### Authorization

No authorization required

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Read-only snapshot of the shared presentation. |  -  |
**400** | Missing token. |  -  |
**401** | Password-protected deck. &#x60;requiresPassword: true&#x60; always set; &#x60;invalidPassword: true&#x60; only when a password was supplied and rejected.  |  -  |
**404** | Token unknown or sharing disabled. |  -  |
**500** | Snapshot rendering failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_slide**
> Slide get_slide(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one slide.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide import Slide
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one slide.
        api_response = api_instance.get_slide(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->get_slide:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->get_slide: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The slide. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Slide not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_slide_element**
> SlideElement get_slide_element(id, slide_id, element_id, account_id=account_id, x_workspace_id=x_workspace_id)

Fetch one slide element.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide_element import SlideElement
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    element_id = 'element_id_example' # str | Slide-element id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Fetch one slide element.
        api_response = api_instance.get_slide_element(id, slide_id, element_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->get_slide_element:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->get_slide_element: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **element_id** | **str**| Slide-element id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The element. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Element not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_presentations**
> PresentationListEnvelope list_presentations(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, limit=limit, offset=offset)

List presentations across connected accounts.

Fan-out list. Returns every presentation visible to the caller
across every connected slides provider. Pass `?accountId=` or
`?provider=` to scope to a single source.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.presentation_list_envelope import PresentationListEnvelope
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
    api_instance = spatio.SlidesApi(api_client)
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    provider = 'provider_example' # str | Provider id (e.g. `native-notes`, `notion`). Selects every connected account for the provider. Mutually exclusive with `accountId`.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)
    limit = 50 # int |  (optional) (default to 50)
    offset = 0 # int |  (optional) (default to 0)

    try:
        # List presentations across connected accounts.
        api_response = api_instance.list_presentations(account_id=account_id, provider=provider, x_workspace_id=x_workspace_id, limit=limit, offset=offset)
        print("The response of SlidesApi->list_presentations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->list_presentations: %s\n" % e)
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

[**PresentationListEnvelope**](PresentationListEnvelope.md)

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

# **list_slide_elements**
> SlideElementList list_slide_elements(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)

List the canvas elements on a slide.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide_element_list import SlideElementList
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # List the canvas elements on a slide.
        api_response = api_instance.list_slide_elements(id, slide_id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->list_slide_elements:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->list_slide_elements: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SlideElementList**](SlideElementList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slide-element list. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Slide not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_slides_in_presentation**
> SlideList list_slides_in_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)

List slides in a presentation.

Single-account list. Returns slides in the order set by their
`position` field.


### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide_list import SlideList
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # List slides in a presentation.
        api_response = api_instance.list_slides_in_presentation(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->list_slides_in_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->list_slides_in_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SlideList**](SlideList.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slide list. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **rotate_presentation_share_token**
> ShareSettings rotate_presentation_share_token(id, account_id=account_id, x_workspace_id=x_workspace_id)

Rotate the share token, invalidating outstanding URLs.

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.share_settings import ShareSettings
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Rotate the share token, invalidating outstanding URLs.
        api_response = api_instance.rotate_presentation_share_token(id, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->rotate_presentation_share_token:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->rotate_presentation_share_token: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**ShareSettings**](ShareSettings.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | New share settings (with the new token + URL). |  -  |
**401** | Caller is not authenticated. |  -  |
**403** | Caller is not the deck owner. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_presentation**
> Presentation update_presentation(id, update_presentation_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update presentation metadata (partial).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.presentation import Presentation
from spatio.models.update_presentation_request import UpdatePresentationRequest
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    update_presentation_request = spatio.UpdatePresentationRequest() # UpdatePresentationRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update presentation metadata (partial).
        api_response = api_instance.update_presentation(id, update_presentation_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->update_presentation:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->update_presentation: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **update_presentation_request** | [**UpdatePresentationRequest**](UpdatePresentationRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Presentation**](Presentation.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated presentation. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Presentation not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_slide**
> Slide update_slide(id, slide_id, update_slide_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a slide (partial).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide import Slide
from spatio.models.update_slide_request import UpdateSlideRequest
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    update_slide_request = spatio.UpdateSlideRequest() # UpdateSlideRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a slide (partial).
        api_response = api_instance.update_slide(id, slide_id, update_slide_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->update_slide:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->update_slide: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **update_slide_request** | [**UpdateSlideRequest**](UpdateSlideRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**Slide**](Slide.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated slide. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Slide not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_slide_element**
> SlideElement update_slide_element(id, slide_id, element_id, update_slide_element_request, account_id=account_id, x_workspace_id=x_workspace_id)

Update a slide element (partial).

### Example

* Bearer (Personal Access Token (pat_...)) Authentication (bearerAuth):

```python
import spatio
from spatio.models.slide_element import SlideElement
from spatio.models.update_slide_element_request import UpdateSlideElementRequest
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
    api_instance = spatio.SlidesApi(api_client)
    id = 'id_example' # str | Presentation id.
    slide_id = 'slide_id_example' # str | Slide id within the presentation.
    element_id = 'element_id_example' # str | Slide-element id.
    update_slide_element_request = spatio.UpdateSlideElementRequest() # UpdateSlideElementRequest | 
    account_id = 'account_id_example' # str | Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with `provider`. If omitted on a list endpoint the call fans out across every connected account.  (optional)
    x_workspace_id = 'x_workspace_id_example' # str | Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  (optional)

    try:
        # Update a slide element (partial).
        api_response = api_instance.update_slide_element(id, slide_id, element_id, update_slide_element_request, account_id=account_id, x_workspace_id=x_workspace_id)
        print("The response of SlidesApi->update_slide_element:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SlidesApi->update_slide_element: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **id** | **str**| Presentation id. | 
 **slide_id** | **str**| Slide id within the presentation. | 
 **element_id** | **str**| Slide-element id. | 
 **update_slide_element_request** | [**UpdateSlideElementRequest**](UpdateSlideElementRequest.md)|  | 
 **account_id** | **str**| Connected-account row id. Selects which provider account this request targets when more than one is connected. Mutually exclusive with &#x60;provider&#x60;. If omitted on a list endpoint the call fans out across every connected account.  | [optional] 
 **x_workspace_id** | **str**| Workspace scope for unscoped tokens. Workspace-scoped PATs and OAuth tokens carry this implicitly; for session/JWT auth without a scoped PAT, pass it explicitly.  | [optional] 

### Return type

[**SlideElement**](SlideElement.md)

### Authorization

[bearerAuth](../README.md#bearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated element. |  -  |
**400** | Invalid body or missing id. |  -  |
**401** | Caller is not authenticated. |  -  |
**404** | Element not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

