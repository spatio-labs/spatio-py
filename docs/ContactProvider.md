# ContactProvider


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**display_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**is_system** | **bool** |  | [optional] 

## Example

```python
from spatio.models.contact_provider import ContactProvider

# TODO update the JSON string below
json = "{}"
# create an instance of ContactProvider from a JSON string
contact_provider_instance = ContactProvider.from_json(json)
# print the JSON string representation of the object
print(ContactProvider.to_json())

# convert the object into a dict
contact_provider_dict = contact_provider_instance.to_dict()
# create an instance of ContactProvider from a dict
contact_provider_from_dict = ContactProvider.from_dict(contact_provider_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


