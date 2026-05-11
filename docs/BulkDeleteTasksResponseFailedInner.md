# BulkDeleteTasksResponseFailedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_id** | **str** |  | 
**error** | **str** |  | 

## Example

```python
from spatio.models.bulk_delete_tasks_response_failed_inner import BulkDeleteTasksResponseFailedInner

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteTasksResponseFailedInner from a JSON string
bulk_delete_tasks_response_failed_inner_instance = BulkDeleteTasksResponseFailedInner.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteTasksResponseFailedInner.to_json())

# convert the object into a dict
bulk_delete_tasks_response_failed_inner_dict = bulk_delete_tasks_response_failed_inner_instance.to_dict()
# create an instance of BulkDeleteTasksResponseFailedInner from a dict
bulk_delete_tasks_response_failed_inner_from_dict = BulkDeleteTasksResponseFailedInner.from_dict(bulk_delete_tasks_response_failed_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


