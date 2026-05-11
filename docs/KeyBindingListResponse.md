# KeyBindingListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bindings** | [**List[KeyBinding]**](KeyBinding.md) |  | 

## Example

```python
from spatio.models.key_binding_list_response import KeyBindingListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of KeyBindingListResponse from a JSON string
key_binding_list_response_instance = KeyBindingListResponse.from_json(json)
# print the JSON string representation of the object
print(KeyBindingListResponse.to_json())

# convert the object into a dict
key_binding_list_response_dict = key_binding_list_response_instance.to_dict()
# create an instance of KeyBindingListResponse from a dict
key_binding_list_response_from_dict = KeyBindingListResponse.from_dict(key_binding_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


