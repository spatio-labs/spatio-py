# TaskComment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**task_id** | **str** |  | 
**content** | **str** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**author** | [**TaskCommentAuthor**](TaskCommentAuthor.md) |  | 

## Example

```python
from spatio.models.task_comment import TaskComment

# TODO update the JSON string below
json = "{}"
# create an instance of TaskComment from a JSON string
task_comment_instance = TaskComment.from_json(json)
# print the JSON string representation of the object
print(TaskComment.to_json())

# convert the object into a dict
task_comment_dict = task_comment_instance.to_dict()
# create an instance of TaskComment from a dict
task_comment_from_dict = TaskComment.from_dict(task_comment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


