# InboxItem

A unified-feed item. Source-aware — `category` indicates which upstream platform (mail, dm, channel, mention, system) produced it; `id` is the inbox-item id (not the underlying message id). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**category** | **str** |  | 
**title** | **str** |  | [optional] 
**snippet** | **str** |  | [optional] 
**source** | **str** |  | [optional] 
**source_id** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**is_read** | **bool** |  | [optional] 
**is_mention** | **bool** |  | [optional] 
**timestamp** | **datetime** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.inbox_item import InboxItem

# TODO update the JSON string below
json = "{}"
# create an instance of InboxItem from a JSON string
inbox_item_instance = InboxItem.from_json(json)
# print the JSON string representation of the object
print(InboxItem.to_json())

# convert the object into a dict
inbox_item_dict = inbox_item_instance.to_dict()
# create an instance of InboxItem from a dict
inbox_item_from_dict = InboxItem.from_dict(inbox_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


