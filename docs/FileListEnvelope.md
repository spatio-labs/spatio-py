# FileListEnvelope

Fan-out list response for `GET /v1/files`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[SpatioFile]**](SpatioFile.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.file_list_envelope import FileListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of FileListEnvelope from a JSON string
file_list_envelope_instance = FileListEnvelope.from_json(json)
# print the JSON string representation of the object
print(FileListEnvelope.to_json())

# convert the object into a dict
file_list_envelope_dict = file_list_envelope_instance.to_dict()
# create an instance of FileListEnvelope from a dict
file_list_envelope_from_dict = FileListEnvelope.from_dict(file_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


