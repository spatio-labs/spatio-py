# OrganizationMemberInvitedBy

Inviter info. Returns either a bare user id (`string`) on legacy paths, or an object envelope `{id, email, name, ...}` on enriched responses. Treat as opaque. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from spatio.models.organization_member_invited_by import OrganizationMemberInvitedBy

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationMemberInvitedBy from a JSON string
organization_member_invited_by_instance = OrganizationMemberInvitedBy.from_json(json)
# print the JSON string representation of the object
print(OrganizationMemberInvitedBy.to_json())

# convert the object into a dict
organization_member_invited_by_dict = organization_member_invited_by_instance.to_dict()
# create an instance of OrganizationMemberInvitedBy from a dict
organization_member_invited_by_from_dict = OrganizationMemberInvitedBy.from_dict(organization_member_invited_by_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


