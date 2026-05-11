# KeyBinding

Merged user-customized key binding.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**action_id** | **str** |  | 
**display_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**key** | **str** |  | [optional] 
**modifiers** | **List[str]** |  | [optional] 
**category** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 
**display_order** | **int** |  | [optional] 
**is_custom** | **bool** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.key_binding import KeyBinding

# TODO update the JSON string below
json = "{}"
# create an instance of KeyBinding from a JSON string
key_binding_instance = KeyBinding.from_json(json)
# print the JSON string representation of the object
print(KeyBinding.to_json())

# convert the object into a dict
key_binding_dict = key_binding_instance.to_dict()
# create an instance of KeyBinding from a dict
key_binding_from_dict = KeyBinding.from_dict(key_binding_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


