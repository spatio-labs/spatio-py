# DMPinnedList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**pinned** | **object** | Provider-shaped pinned list. | [optional] 

## Example

```python
from spatio.models.dm_pinned_list import DMPinnedList

# TODO update the JSON string below
json = "{}"
# create an instance of DMPinnedList from a JSON string
dm_pinned_list_instance = DMPinnedList.from_json(json)
# print the JSON string representation of the object
print(DMPinnedList.to_json())

# convert the object into a dict
dm_pinned_list_dict = dm_pinned_list_instance.to_dict()
# create an instance of DMPinnedList from a dict
dm_pinned_list_from_dict = DMPinnedList.from_dict(dm_pinned_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


