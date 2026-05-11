# Organization

Organization summary used in list responses (`GET /v1/organizations`, `GET /v1/organizations/{id}/workspaces`). Returned with camelCase field names.  NB: The single-org GET `/v1/organizations/{id}` returns a *different shape* (`OrganizationDetailLegacy`, PascalCase keys) today — see that schema for the wire-level reality. This is a known inconsistency the platform-service is expected to converge on the camelCase shape in a future cleanup. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**slug** | **str** |  | 
**description** | **str** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**role** | **str** | The caller&#39;s role in this org (&#x60;owner&#x60;, &#x60;admin&#x60;, &#x60;billing_admin&#x60;, &#x60;member&#x60;). | 
**member_count** | **int** |  | [optional] 
**workspace_count** | **int** |  | [optional] 
**workspaces** | [**List[OrganizationWorkspacesInner]**](OrganizationWorkspacesInner.md) | Compact workspace summaries embedded in the org-list response. | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.organization import Organization

# TODO update the JSON string below
json = "{}"
# create an instance of Organization from a JSON string
organization_instance = Organization.from_json(json)
# print the JSON string representation of the object
print(Organization.to_json())

# convert the object into a dict
organization_dict = organization_instance.to_dict()
# create an instance of Organization from a dict
organization_from_dict = Organization.from_dict(organization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


