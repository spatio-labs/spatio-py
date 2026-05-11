# TaskCommentAuthor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**email** | **str** |  | 
**profile_photo** | **str** |  | [optional] 

## Example

```python
from spatio.models.task_comment_author import TaskCommentAuthor

# TODO update the JSON string below
json = "{}"
# create an instance of TaskCommentAuthor from a JSON string
task_comment_author_instance = TaskCommentAuthor.from_json(json)
# print the JSON string representation of the object
print(TaskCommentAuthor.to_json())

# convert the object into a dict
task_comment_author_dict = task_comment_author_instance.to_dict()
# create an instance of TaskCommentAuthor from a dict
task_comment_author_from_dict = TaskCommentAuthor.from_dict(task_comment_author_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


