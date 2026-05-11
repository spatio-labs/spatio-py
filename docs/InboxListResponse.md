# InboxListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[InboxItem]**](InboxItem.md) |  | 
**total_count** | **int** |  | 
**has_more** | **bool** |  | 

## Example

```python
from spatio.models.inbox_list_response import InboxListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of InboxListResponse from a JSON string
inbox_list_response_instance = InboxListResponse.from_json(json)
# print the JSON string representation of the object
print(InboxListResponse.to_json())

# convert the object into a dict
inbox_list_response_dict = inbox_list_response_instance.to_dict()
# create an instance of InboxListResponse from a dict
inbox_list_response_from_dict = InboxListResponse.from_dict(inbox_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


