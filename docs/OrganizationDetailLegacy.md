# OrganizationDetailLegacy

Single-organization GET response. **PascalCase keys** — inconsistent with the rest of the API (anonymous-struct json-marshal in handler with no field tags). Documented as-is; a future cleanup pass will move this to camelCase via a versioned migration. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**slug** | **str** |  | 
**description** | **str** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**settings** | **str** | JSON-encoded settings string. Parse client-side. | [optional] 
**subscription_tier** | **str** |  | 
**deployment_type** | **str** |  | 
**subscription_status** | **str** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.organization_detail_legacy import OrganizationDetailLegacy

# TODO update the JSON string below
json = "{}"
# create an instance of OrganizationDetailLegacy from a JSON string
organization_detail_legacy_instance = OrganizationDetailLegacy.from_json(json)
# print the JSON string representation of the object
print(OrganizationDetailLegacy.to_json())

# convert the object into a dict
organization_detail_legacy_dict = organization_detail_legacy_instance.to_dict()
# create an instance of OrganizationDetailLegacy from a dict
organization_detail_legacy_from_dict = OrganizationDetailLegacy.from_dict(organization_detail_legacy_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


