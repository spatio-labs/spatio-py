# UpdateContactCategoryRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**color** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_contact_category_request import UpdateContactCategoryRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateContactCategoryRequest from a JSON string
update_contact_category_request_instance = UpdateContactCategoryRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateContactCategoryRequest.to_json())

# convert the object into a dict
update_contact_category_request_dict = update_contact_category_request_instance.to_dict()
# create an instance of UpdateContactCategoryRequest from a dict
update_contact_category_request_from_dict = UpdateContactCategoryRequest.from_dict(update_contact_category_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


