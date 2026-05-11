# UpdateWorkspaceMemberRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 

## Example

```python
from spatio.models.update_workspace_member_request import UpdateWorkspaceMemberRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateWorkspaceMemberRequest from a JSON string
update_workspace_member_request_instance = UpdateWorkspaceMemberRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateWorkspaceMemberRequest.to_json())

# convert the object into a dict
update_workspace_member_request_dict = update_workspace_member_request_instance.to_dict()
# create an instance of UpdateWorkspaceMemberRequest from a dict
update_workspace_member_request_from_dict = UpdateWorkspaceMemberRequest.from_dict(update_workspace_member_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


