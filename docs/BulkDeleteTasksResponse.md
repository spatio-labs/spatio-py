# BulkDeleteTasksResponse

Partial-success envelope. `success` is `true` only when zero failures; `affectedCount` is the deleted count; `taskIds` lists the ids that succeeded; `failed` lists per-id errors. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**affected_count** | **int** |  | 
**task_ids** | **List[str]** |  | 
**failed** | [**List[BulkDeleteTasksResponseFailedInner]**](BulkDeleteTasksResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_delete_tasks_response import BulkDeleteTasksResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteTasksResponse from a JSON string
bulk_delete_tasks_response_instance = BulkDeleteTasksResponse.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteTasksResponse.to_json())

# convert the object into a dict
bulk_delete_tasks_response_dict = bulk_delete_tasks_response_instance.to_dict()
# create an instance of BulkDeleteTasksResponse from a dict
bulk_delete_tasks_response_from_dict = BulkDeleteTasksResponse.from_dict(bulk_delete_tasks_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


