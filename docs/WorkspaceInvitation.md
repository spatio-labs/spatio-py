# WorkspaceInvitation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**workspace_id** | **str** |  | [optional] 
**email** | **str** |  | 
**role** | **str** |  | 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**accepted_at** | **datetime** |  | [optional] 
**revoked_at** | **datetime** |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from spatio.models.workspace_invitation import WorkspaceInvitation

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceInvitation from a JSON string
workspace_invitation_instance = WorkspaceInvitation.from_json(json)
# print the JSON string representation of the object
print(WorkspaceInvitation.to_json())

# convert the object into a dict
workspace_invitation_dict = workspace_invitation_instance.to_dict()
# create an instance of WorkspaceInvitation from a dict
workspace_invitation_from_dict = WorkspaceInvitation.from_dict(workspace_invitation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


