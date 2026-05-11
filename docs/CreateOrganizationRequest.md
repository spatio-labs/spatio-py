# CreateOrganizationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**slug** | **str** | Auto-generated from &#x60;name&#x60; if omitted. Slug collisions are auto-suffixed with &#x60;-2&#x60;, &#x60;-3&#x60;, etc.  | [optional] 
**description** | **str** |  | [optional] 
**logo_url** | **str** |  | [optional] 
**create_default_workspace** | **bool** | &#x60;true&#x60; (default) creates a default workspace alongside the org. | [optional] 
**default_workspace_name** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_organization_request import CreateOrganizationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateOrganizationRequest from a JSON string
create_organization_request_instance = CreateOrganizationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateOrganizationRequest.to_json())

# convert the object into a dict
create_organization_request_dict = create_organization_request_instance.to_dict()
# create an instance of CreateOrganizationRequest from a dict
create_organization_request_from_dict = CreateOrganizationRequest.from_dict(create_organization_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


