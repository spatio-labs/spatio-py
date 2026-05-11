# ExecuteActionRequest

Generic action-execute payload. Tool-specific shape lives in `params`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action_id** | **str** |  | 
**params** | **Dict[str, object]** |  | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.execute_action_request import ExecuteActionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ExecuteActionRequest from a JSON string
execute_action_request_instance = ExecuteActionRequest.from_json(json)
# print the JSON string representation of the object
print(ExecuteActionRequest.to_json())

# convert the object into a dict
execute_action_request_dict = execute_action_request_instance.to_dict()
# create an instance of ExecuteActionRequest from a dict
execute_action_request_from_dict = ExecuteActionRequest.from_dict(execute_action_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


