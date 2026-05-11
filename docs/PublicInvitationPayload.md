# PublicInvitationPayload

Returned by `GET /invitations/{token}` (unauthenticated). Lets the renderer show invitation details (workspace name, inviter, role) before the user signs in. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **str** |  | 
**id** | **str** |  | 
**workspace_id** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 
**email** | **str** |  | 
**role** | **str** |  | 
**status** | **str** |  | 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**workspace** | **Dict[str, object]** |  | [optional] 
**organization** | **Dict[str, object]** |  | [optional] 
**invited_by** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.public_invitation_payload import PublicInvitationPayload

# TODO update the JSON string below
json = "{}"
# create an instance of PublicInvitationPayload from a JSON string
public_invitation_payload_instance = PublicInvitationPayload.from_json(json)
# print the JSON string representation of the object
print(PublicInvitationPayload.to_json())

# convert the object into a dict
public_invitation_payload_dict = public_invitation_payload_instance.to_dict()
# create an instance of PublicInvitationPayload from a dict
public_invitation_payload_from_dict = PublicInvitationPayload.from_dict(public_invitation_payload_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


