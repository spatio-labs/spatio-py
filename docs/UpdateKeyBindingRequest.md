# UpdateKeyBindingRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**modifiers** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.update_key_binding_request import UpdateKeyBindingRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateKeyBindingRequest from a JSON string
update_key_binding_request_instance = UpdateKeyBindingRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateKeyBindingRequest.to_json())

# convert the object into a dict
update_key_binding_request_dict = update_key_binding_request_instance.to_dict()
# create an instance of UpdateKeyBindingRequest from a dict
update_key_binding_request_from_dict = UpdateKeyBindingRequest.from_dict(update_key_binding_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


