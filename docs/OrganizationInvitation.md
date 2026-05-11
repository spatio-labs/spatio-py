# OrganizationInvitation


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**organization_id** | **str** |  | [optional] 
**email** | **str** |  | 
**role** | **str** |  | 
**token** | **str** | Opaque invitation token (omitted on list responses). | [optional] 
**expires_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**accepted_at** | **datetime** |  | [optional] 
**revoked_at** | **datetime** |  | [optional] 
**invited_by** | [**OrganizationMemberInvitedBy**](OrganizationMemberInvitedBy.md) |  | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from spatio.models.organization_invitation import OrganizationInvitation

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationInvitation from a JSON string
organization_invitation_instance = OrganizationInvitation.from_json(json)
# print the JSON string representation of the object
print(OrganizationInvitation.to_json())

# convert the object into a dict
organization_invitation_dict = organization_invitation_instance.to_dict()
# create an instance of OrganizationInvitation from a dict
organization_invitation_from_dict = OrganizationInvitation.from_dict(organization_invitation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


