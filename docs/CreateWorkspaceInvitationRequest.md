# CreateWorkspaceInvitationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**role** | **str** |  | 

## Example

```python
from spatio.models.create_workspace_invitation_request import CreateWorkspaceInvitationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateWorkspaceInvitationRequest from a JSON string
create_workspace_invitation_request_instance = CreateWorkspaceInvitationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateWorkspaceInvitationRequest.to_json())

# convert the object into a dict
create_workspace_invitation_request_dict = create_workspace_invitation_request_instance.to_dict()
# create an instance of CreateWorkspaceInvitationRequest from a dict
create_workspace_invitation_request_from_dict = CreateWorkspaceInvitationRequest.from_dict(create_workspace_invitation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


