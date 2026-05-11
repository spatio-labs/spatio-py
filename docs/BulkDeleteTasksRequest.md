# BulkDeleteTasksRequest

Either populate `taskIds` (with optional parallel `accountIds`) for multi-task delete, or `taskId` (with optional `accountId`) for the single-task fallback. `taskIds` wins when both are set. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_ids** | **List[str]** |  | [optional] 
**account_ids** | **List[str]** | Parallel slice with taskIds — accountIds[i] targets taskIds[i]. | [optional] 
**task_id** | **str** | Singular fallback when only deleting one task. | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.bulk_delete_tasks_request import BulkDeleteTasksRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteTasksRequest from a JSON string
bulk_delete_tasks_request_instance = BulkDeleteTasksRequest.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteTasksRequest.to_json())

# convert the object into a dict
bulk_delete_tasks_request_dict = bulk_delete_tasks_request_instance.to_dict()
# create an instance of BulkDeleteTasksRequest from a dict
bulk_delete_tasks_request_from_dict = BulkDeleteTasksRequest.from_dict(bulk_delete_tasks_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


