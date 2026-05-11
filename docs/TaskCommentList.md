# TaskCommentList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comments** | [**List[TaskComment]**](TaskComment.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.task_comment_list import TaskCommentList

# TODO update the JSON string below
json = "{}"
# create an instance of TaskCommentList from a JSON string
task_comment_list_instance = TaskCommentList.from_json(json)
# print the JSON string representation of the object
print(TaskCommentList.to_json())

# convert the object into a dict
task_comment_list_dict = task_comment_list_instance.to_dict()
# create an instance of TaskCommentList from a dict
task_comment_list_from_dict = TaskCommentList.from_dict(task_comment_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


