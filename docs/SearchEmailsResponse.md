# SearchEmailsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emails** | [**List[Email]**](Email.md) | &#x60;null&#x60; when there are no results (Go nil-slice serialization). Treat as equivalent to an empty array.  | [optional] 
**total** | **int** |  | 
**next_page_token** | **str** |  | [optional] 
**provider** | **str** |  | 

## Example

```python
from spatio.models.search_emails_response import SearchEmailsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchEmailsResponse from a JSON string
search_emails_response_instance = SearchEmailsResponse.from_json(json)
# print the JSON string representation of the object
print(SearchEmailsResponse.to_json())

# convert the object into a dict
search_emails_response_dict = search_emails_response_instance.to_dict()
# create an instance of SearchEmailsResponse from a dict
search_emails_response_from_dict = SearchEmailsResponse.from_dict(search_emails_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


