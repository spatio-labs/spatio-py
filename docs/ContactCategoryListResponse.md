# ContactCategoryListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**categories** | [**List[ContactCategory]**](ContactCategory.md) |  | 

## Example

```python
from spatio.models.contact_category_list_response import ContactCategoryListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ContactCategoryListResponse from a JSON string
contact_category_list_response_instance = ContactCategoryListResponse.from_json(json)
# print the JSON string representation of the object
print(ContactCategoryListResponse.to_json())

# convert the object into a dict
contact_category_list_response_dict = contact_category_list_response_instance.to_dict()
# create an instance of ContactCategoryListResponse from a dict
contact_category_list_response_from_dict = ContactCategoryListResponse.from_dict(contact_category_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


