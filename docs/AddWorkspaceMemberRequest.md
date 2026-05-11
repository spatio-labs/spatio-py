# AddWorkspaceMemberRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**role** | **str** |  | 

## Example

```python
from spatio.models.add_workspace_member_request import AddWorkspaceMemberRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AddWorkspaceMemberRequest from a JSON string
add_workspace_member_request_instance = AddWorkspaceMemberRequest.from_json(json)
# print the JSON string representation of the object
print(AddWorkspaceMemberRequest.to_json())

# convert the object into a dict
add_workspace_member_request_dict = add_workspace_member_request_instance.to_dict()
# create an instance of AddWorkspaceMemberRequest from a dict
add_workspace_member_request_from_dict = AddWorkspaceMemberRequest.from_dict(add_workspace_member_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


