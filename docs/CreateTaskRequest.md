# CreateTaskRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**due_date** | **datetime** |  | [optional] 
**priority** | **str** |  | [optional] 
**labels** | **List[str]** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**assignee_id** | **str** |  | [optional] 
**parent_task_id** | **str** |  | [optional] 
**type** | **str** |  | [optional] 
**source_platform** | **str** |  | [optional] 
**source_id** | **str** |  | [optional] 
**account_id** | **str** | Optional override for the target connected account. May also be passed as &#x60;?accountId&#x3D;&#x60;.  | [optional] 
**provider** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_task_request import CreateTaskRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateTaskRequest from a JSON string
create_task_request_instance = CreateTaskRequest.from_json(json)
# print the JSON string representation of the object
print(CreateTaskRequest.to_json())

# convert the object into a dict
create_task_request_dict = create_task_request_instance.to_dict()
# create an instance of CreateTaskRequest from a dict
create_task_request_from_dict = CreateTaskRequest.from_dict(create_task_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


