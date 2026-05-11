# WorkspaceEnvelope


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workspace** | [**Workspace**](Workspace.md) |  | 

## Example

```python
from spatio.models.workspace_envelope import WorkspaceEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceEnvelope from a JSON string
workspace_envelope_instance = WorkspaceEnvelope.from_json(json)
# print the JSON string representation of the object
print(WorkspaceEnvelope.to_json())

# convert the object into a dict
workspace_envelope_dict = workspace_envelope_instance.to_dict()
# create an instance of WorkspaceEnvelope from a dict
workspace_envelope_from_dict = WorkspaceEnvelope.from_dict(workspace_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


