# ConnectedAppItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** |  | 
**client_name** | **str** |  | 
**logo_uri** | **str** |  | [optional] 
**client_uri** | **str** |  | [optional] 
**policy_uri** | **str** |  | [optional] 
**tos_uri** | **str** |  | [optional] 
**scopes** | **List[str]** |  | 
**scope_labels** | **List[str]** |  | 
**granted_at** | **datetime** |  | 

## Example

```python
from spatio.models.connected_app_item import ConnectedAppItem

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectedAppItem from a JSON string
connected_app_item_instance = ConnectedAppItem.from_json(json)
# print the JSON string representation of the object
print(ConnectedAppItem.to_json())

# convert the object into a dict
connected_app_item_dict = connected_app_item_instance.to_dict()
# create an instance of ConnectedAppItem from a dict
connected_app_item_from_dict = ConnectedAppItem.from_dict(connected_app_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


