# ConsumeAgentTaskResponse

Atomic check+increment. Returns the updated counter on success; returns 402 on `trial_expired` and 429 on `daily_limit_exceeded` (the body in error cases is the `ApiError` envelope). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**allowed** | **bool** |  | 
**task_count** | **int** |  | [optional] 
**daily_limit** | **int** |  | [optional] 
**trial_ends_at** | **datetime** |  | [optional] 
**paid** | **bool** |  | [optional] 

## Example

```python
from spatio.models.consume_agent_task_response import ConsumeAgentTaskResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ConsumeAgentTaskResponse from a JSON string
consume_agent_task_response_instance = ConsumeAgentTaskResponse.from_json(json)
# print the JSON string representation of the object
print(ConsumeAgentTaskResponse.to_json())

# convert the object into a dict
consume_agent_task_response_dict = consume_agent_task_response_instance.to_dict()
# create an instance of ConsumeAgentTaskResponse from a dict
consume_agent_task_response_from_dict = ConsumeAgentTaskResponse.from_dict(consume_agent_task_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


