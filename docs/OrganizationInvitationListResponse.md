# OrganizationInvitationListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**invitations** | [**List[OrganizationInvitation]**](OrganizationInvitation.md) |  | 

## Example

```python
from spatio.models.organization_invitation_list_response import OrganizationInvitationListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationInvitationListResponse from a JSON string
organization_invitation_list_response_instance = OrganizationInvitationListResponse.from_json(json)
# print the JSON string representation of the object
print(OrganizationInvitationListResponse.to_json())

# convert the object into a dict
organization_invitation_list_response_dict = organization_invitation_list_response_instance.to_dict()
# create an instance of OrganizationInvitationListResponse from a dict
organization_invitation_list_response_from_dict = OrganizationInvitationListResponse.from_dict(organization_invitation_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


