# ContactCategory


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**color** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.contact_category import ContactCategory

# TODO update the JSON string below
json = "{}"
# create an instance of ContactCategory from a JSON string
contact_category_instance = ContactCategory.from_json(json)
# print the JSON string representation of the object
print(ContactCategory.to_json())

# convert the object into a dict
contact_category_dict = contact_category_instance.to_dict()
# create an instance of ContactCategory from a dict
contact_category_from_dict = ContactCategory.from_dict(contact_category_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


