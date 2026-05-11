# ValidateKeyBindingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action_id** | **str** |  | 
**key** | **str** |  | 
**modifiers** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.validate_key_binding_request import ValidateKeyBindingRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ValidateKeyBindingRequest from a JSON string
validate_key_binding_request_instance = ValidateKeyBindingRequest.from_json(json)
# print the JSON string representation of the object
print(ValidateKeyBindingRequest.to_json())

# convert the object into a dict
validate_key_binding_request_dict = validate_key_binding_request_instance.to_dict()
# create an instance of ValidateKeyBindingRequest from a dict
validate_key_binding_request_from_dict = ValidateKeyBindingRequest.from_dict(validate_key_binding_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


