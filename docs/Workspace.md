# Workspace

A workspace within an organization. Returned in list responses (`GET /v1/workspaces`, `GET /v1/organizations/{id}/workspaces`) and the single-get response (`GET /v1/workspaces/{id}`, wrapped in `{workspace: ...}`).  `settings` shape varies by endpoint — sometimes a JSON object, sometimes a JSON-encoded string. Treat as opaque. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**slug** | **str** |  | 
**description** | **str** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 
**organization** | [**WorkspaceOrganization**](WorkspaceOrganization.md) |  | [optional] 
**role** | **str** | The caller&#39;s role in this workspace (&#x60;owner&#x60;, &#x60;admin&#x60;, &#x60;member&#x60;, &#x60;guest&#x60;). | [optional] 
**settings** | **object** | Per-workspace settings. Currently emitted as either an object (&#x60;{language, timezone, ...}&#x60;) on &#x60;GET /v1/workspaces/{id}&#x60; or a JSON-encoded string on &#x60;GET /v1/organizations/{id}/workspaces&#x60;. Treat as opaque and parse defensively.  | [optional] 
**is_default** | **bool** |  | [optional] 
**member_count** | **int** |  | [optional] 
**billing_tier** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.workspace import Workspace

# TODO update the JSON string below
json = "{}"
# create an instance of Workspace from a JSON string
workspace_instance = Workspace.from_json(json)
# print the JSON string representation of the object
print(Workspace.to_json())

# convert the object into a dict
workspace_dict = workspace_instance.to_dict()
# create an instance of Workspace from a dict
workspace_from_dict = Workspace.from_dict(workspace_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


