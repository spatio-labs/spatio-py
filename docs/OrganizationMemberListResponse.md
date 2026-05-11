# OrganizationMemberListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**members** | [**List[OrganizationMember]**](OrganizationMember.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.organization_member_list_response import OrganizationMemberListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationMemberListResponse from a JSON string
organization_member_list_response_instance = OrganizationMemberListResponse.from_json(json)
# print the JSON string representation of the object
print(OrganizationMemberListResponse.to_json())

# convert the object into a dict
organization_member_list_response_dict = organization_member_list_response_instance.to_dict()
# create an instance of OrganizationMemberListResponse from a dict
organization_member_list_response_from_dict = OrganizationMemberListResponse.from_dict(organization_member_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


