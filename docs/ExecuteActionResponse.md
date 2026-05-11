# ExecuteActionResponse

Generic action-execute result envelope. Tool-specific shape lives in `data`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ok** | **bool** |  | [optional] 
**data** | **Dict[str, object]** |  | [optional] 
**error** | **str** |  | [optional] 

## Example

```python
from spatio.models.execute_action_response import ExecuteActionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ExecuteActionResponse from a JSON string
execute_action_response_instance = ExecuteActionResponse.from_json(json)
# print the JSON string representation of the object
print(ExecuteActionResponse.to_json())

# convert the object into a dict
execute_action_response_dict = execute_action_response_instance.to_dict()
# create an instance of ExecuteActionResponse from a dict
execute_action_response_from_dict = ExecuteActionResponse.from_dict(execute_action_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


