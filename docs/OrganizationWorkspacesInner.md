# OrganizationWorkspacesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**slug** | **str** |  | 

## Example

```python
from spatio.models.organization_workspaces_inner import OrganizationWorkspacesInner

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationWorkspacesInner from a JSON string
organization_workspaces_inner_instance = OrganizationWorkspacesInner.from_json(json)
# print the JSON string representation of the object
print(OrganizationWorkspacesInner.to_json())

# convert the object into a dict
organization_workspaces_inner_dict = organization_workspaces_inner_instance.to_dict()
# create an instance of OrganizationWorkspacesInner from a dict
organization_workspaces_inner_from_dict = OrganizationWorkspacesInner.from_dict(organization_workspaces_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


