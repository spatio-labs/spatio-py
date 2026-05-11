# TaskListEnvelope

Fan-out response for `GET /v1/tasks`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Task]**](Task.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.task_list_envelope import TaskListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of TaskListEnvelope from a JSON string
task_list_envelope_instance = TaskListEnvelope.from_json(json)
# print the JSON string representation of the object
print(TaskListEnvelope.to_json())

# convert the object into a dict
task_list_envelope_dict = task_list_envelope_instance.to_dict()
# create an instance of TaskListEnvelope from a dict
task_list_envelope_from_dict = TaskListEnvelope.from_dict(task_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


