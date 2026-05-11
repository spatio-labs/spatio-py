# InboxCounts


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**mentions** | **int** |  | 
**notifications** | **int** |  | 

## Example

```python
from spatio.models.inbox_counts import InboxCounts

# TODO update the JSON string below
json = "{}"
# create an instance of InboxCounts from a JSON string
inbox_counts_instance = InboxCounts.from_json(json)
# print the JSON string representation of the object
print(InboxCounts.to_json())

# convert the object into a dict
inbox_counts_dict = inbox_counts_instance.to_dict()
# create an instance of InboxCounts from a dict
inbox_counts_from_dict = InboxCounts.from_dict(inbox_counts_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


