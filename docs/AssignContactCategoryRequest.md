# AssignContactCategoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**category_id** | **str** |  | 

## Example

```python
from spatio.models.assign_contact_category_request import AssignContactCategoryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AssignContactCategoryRequest from a JSON string
assign_contact_category_request_instance = AssignContactCategoryRequest.from_json(json)
# print the JSON string representation of the object
print(AssignContactCategoryRequest.to_json())

# convert the object into a dict
assign_contact_category_request_dict = assign_contact_category_request_instance.to_dict()
# create an instance of AssignContactCategoryRequest from a dict
assign_contact_category_request_from_dict = AssignContactCategoryRequest.from_dict(assign_contact_category_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


