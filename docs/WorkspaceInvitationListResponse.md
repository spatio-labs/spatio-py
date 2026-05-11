# WorkspaceInvitationListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invitations** | [**List[WorkspaceInvitation]**](WorkspaceInvitation.md) |  | 

## Example

```python
from spatio.models.workspace_invitation_list_response import WorkspaceInvitationListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceInvitationListResponse from a JSON string
workspace_invitation_list_response_instance = WorkspaceInvitationListResponse.from_json(json)
# print the JSON string representation of the object
print(WorkspaceInvitationListResponse.to_json())

# convert the object into a dict
workspace_invitation_list_response_dict = workspace_invitation_list_response_instance.to_dict()
# create an instance of WorkspaceInvitationListResponse from a dict
workspace_invitation_list_response_from_dict = WorkspaceInvitationListResponse.from_dict(workspace_invitation_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


