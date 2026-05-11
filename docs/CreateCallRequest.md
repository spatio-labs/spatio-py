# CreateCallRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**room_id** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_call_request import CreateCallRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCallRequest from a JSON string
create_call_request_instance = CreateCallRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCallRequest.to_json())

# convert the object into a dict
create_call_request_dict = create_call_request_instance.to_dict()
# create an instance of CreateCallRequest from a dict
create_call_request_from_dict = CreateCallRequest.from_dict(create_call_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


