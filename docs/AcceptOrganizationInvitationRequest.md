# AcceptOrganizationInvitationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | 

## Example

```python
from spatio.models.accept_organization_invitation_request import AcceptOrganizationInvitationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AcceptOrganizationInvitationRequest from a JSON string
accept_organization_invitation_request_instance = AcceptOrganizationInvitationRequest.from_json(json)
# print the JSON string representation of the object
print(AcceptOrganizationInvitationRequest.to_json())

# convert the object into a dict
accept_organization_invitation_request_dict = accept_organization_invitation_request_instance.to_dict()
# create an instance of AcceptOrganizationInvitationRequest from a dict
accept_organization_invitation_request_from_dict = AcceptOrganizationInvitationRequest.from_dict(accept_organization_invitation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


