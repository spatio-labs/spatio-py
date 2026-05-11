# AgentTaskUsage

Free-trial agent-task gate. `allowed` is the only field clients must check before issuing a turn. Paid users get `paid: true, allowed: true` with the count fields null. 

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
from spatio.models.agent_task_usage import AgentTaskUsage

# TODO update the JSON string below
json = "{}"
# create an instance of AgentTaskUsage from a JSON string
agent_task_usage_instance = AgentTaskUsage.from_json(json)
# print the JSON string representation of the object
print(AgentTaskUsage.to_json())

# convert the object into a dict
agent_task_usage_dict = agent_task_usage_instance.to_dict()
# create an instance of AgentTaskUsage from a dict
agent_task_usage_from_dict = AgentTaskUsage.from_dict(agent_task_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


