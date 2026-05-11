# WorkspaceMember


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**role** | **str** |  | 
**email** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**avatar** | **str** |  | [optional] 
**joined_at** | **datetime** |  | 
**user** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.workspace_member import WorkspaceMember

# TODO update the JSON string below
json = "{}"
# create an instance of WorkspaceMember from a JSON string
workspace_member_instance = WorkspaceMember.from_json(json)
# print the JSON string representation of the object
print(WorkspaceMember.to_json())

# convert the object into a dict
workspace_member_dict = workspace_member_instance.to_dict()
# create an instance of WorkspaceMember from a dict
workspace_member_from_dict = WorkspaceMember.from_dict(workspace_member_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


