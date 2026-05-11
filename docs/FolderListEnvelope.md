# FolderListEnvelope

Fan-out list response for `GET /v1/files/folders`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Folder]**](Folder.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.folder_list_envelope import FolderListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of FolderListEnvelope from a JSON string
folder_list_envelope_instance = FolderListEnvelope.from_json(json)
# print the JSON string representation of the object
print(FolderListEnvelope.to_json())

# convert the object into a dict
folder_list_envelope_dict = folder_list_envelope_instance.to_dict()
# create an instance of FolderListEnvelope from a dict
folder_list_envelope_from_dict = FolderListEnvelope.from_dict(folder_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


