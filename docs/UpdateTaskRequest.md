# UpdateTaskRequest

Partial update — every field is optional. `dueDate` and `parentTaskId` are nullable: send `null` to clear, omit to leave untouched, send a value to set. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**due_date** | **datetime** |  | [optional] 
**priority** | **str** |  | [optional] 
**labels** | **List[str]** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**assignee_id** | **str** |  | [optional] 
**parent_task_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_task_request import UpdateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateTaskRequest from a JSON string
update_task_request_instance = UpdateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateTaskRequest.to_json())

# convert the object into a dict
update_task_request_dict = update_task_request_instance.to_dict()
# create an instance of UpdateTaskRequest from a dict
update_task_request_from_dict = UpdateTaskRequest.from_dict(update_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


