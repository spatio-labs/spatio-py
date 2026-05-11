# CreateContactCategoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**color** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_contact_category_request import CreateContactCategoryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateContactCategoryRequest from a JSON string
create_contact_category_request_instance = CreateContactCategoryRequest.from_json(json)
# print the JSON string representation of the object
print(CreateContactCategoryRequest.to_json())

# convert the object into a dict
create_contact_category_request_dict = create_contact_category_request_instance.to_dict()
# create an instance of CreateContactCategoryRequest from a dict
create_contact_category_request_from_dict = CreateContactCategoryRequest.from_dict(create_contact_category_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


