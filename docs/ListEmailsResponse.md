# ListEmailsResponse

List of emails across the selected accounts. `provider` is set on single-account calls; on fan-out it carries the value from the first contributing account (legacy behavior — clients should rely on the per-row `provider` field instead). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emails** | [**List[Email]**](Email.md) | &#x60;null&#x60; when there are no results (Go nil-slice serialization). Treat as equivalent to an empty array.  | [optional] 
**total** | **int** |  | 
**next_page_token** | **str** |  | [optional] 
**provider** | **str** |  | 

## Example

```python
from spatio.models.list_emails_response import ListEmailsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListEmailsResponse from a JSON string
list_emails_response_instance = ListEmailsResponse.from_json(json)
# print the JSON string representation of the object
print(ListEmailsResponse.to_json())

# convert the object into a dict
list_emails_response_dict = list_emails_response_instance.to_dict()
# create an instance of ListEmailsResponse from a dict
list_emails_response_from_dict = ListEmailsResponse.from_dict(list_emails_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


