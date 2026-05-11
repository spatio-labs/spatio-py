# BulkUpdateTasksRequest

Apply the same `updates` payload to every id. Same parallel AccountIDs convention as bulk delete. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_ids** | **List[str]** |  | 
**account_ids** | **List[str]** |  | [optional] 
**account_id** | **str** |  | [optional] 
**updates** | [**UpdateTaskRequest**](UpdateTaskRequest.md) |  | 

## Example

```python
from spatio.models.bulk_update_tasks_request import BulkUpdateTasksRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkUpdateTasksRequest from a JSON string
bulk_update_tasks_request_instance = BulkUpdateTasksRequest.from_json(json)
# print the JSON string representation of the object
print(BulkUpdateTasksRequest.to_json())

# convert the object into a dict
bulk_update_tasks_request_dict = bulk_update_tasks_request_instance.to_dict()
# create an instance of BulkUpdateTasksRequest from a dict
bulk_update_tasks_request_from_dict = BulkUpdateTasksRequest.from_dict(bulk_update_tasks_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


