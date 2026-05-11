# ValidateKeyBindingResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **bool** |  | 
**conflicts** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.validate_key_binding_response import ValidateKeyBindingResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ValidateKeyBindingResponse from a JSON string
validate_key_binding_response_instance = ValidateKeyBindingResponse.from_json(json)
# print the JSON string representation of the object
print(ValidateKeyBindingResponse.to_json())

# convert the object into a dict
validate_key_binding_response_dict = validate_key_binding_response_instance.to_dict()
# create an instance of ValidateKeyBindingResponse from a dict
validate_key_binding_response_from_dict = ValidateKeyBindingResponse.from_dict(validate_key_binding_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


