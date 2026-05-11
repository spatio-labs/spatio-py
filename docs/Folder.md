# Folder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**parent_id** | **str** |  | [optional] 
**path** | **str** | Display path from the root (e.g. &#x60;/Finance/Q3&#x60;). | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.folder import Folder

# TODO update the JSON string below
json = "{}"
# create an instance of Folder from a JSON string
folder_instance = Folder.from_json(json)
# print the JSON string representation of the object
print(Folder.to_json())

# convert the object into a dict
folder_dict = folder_instance.to_dict()
# create an instance of Folder from a dict
folder_from_dict = Folder.from_dict(folder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


