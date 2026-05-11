# BulkUpdateTasksResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**affected_count** | **int** |  | 
**tasks** | [**List[Task]**](Task.md) |  | 
**failed** | [**List[BulkDeleteTasksResponseFailedInner]**](BulkDeleteTasksResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_update_tasks_response import BulkUpdateTasksResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkUpdateTasksResponse from a JSON string
bulk_update_tasks_response_instance = BulkUpdateTasksResponse.from_json(json)
# print the JSON string representation of the object
print(BulkUpdateTasksResponse.to_json())

# convert the object into a dict
bulk_update_tasks_response_dict = bulk_update_tasks_response_instance.to_dict()
# create an instance of BulkUpdateTasksResponse from a dict
bulk_update_tasks_response_from_dict = BulkUpdateTasksResponse.from_dict(bulk_update_tasks_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


