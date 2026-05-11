# UpdateOrganizationMemberRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 

## Example

```python
from spatio.models.update_organization_member_request import UpdateOrganizationMemberRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateOrganizationMemberRequest from a JSON string
update_organization_member_request_instance = UpdateOrganizationMemberRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateOrganizationMemberRequest.to_json())

# convert the object into a dict
update_organization_member_request_dict = update_organization_member_request_instance.to_dict()
# create an instance of UpdateOrganizationMemberRequest from a dict
update_organization_member_request_from_dict = UpdateOrganizationMemberRequest.from_dict(update_organization_member_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


