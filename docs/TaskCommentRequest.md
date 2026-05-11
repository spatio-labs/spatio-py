# TaskCommentRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** |  | 

## Example

```python
from spatio.models.task_comment_request import TaskCommentRequest

# TODO update the JSON string below
json = "{}"
# create an instance of TaskCommentRequest from a JSON string
task_comment_request_instance = TaskCommentRequest.from_json(json)
# print the JSON string representation of the object
print(TaskCommentRequest.to_json())

# convert the object into a dict
task_comment_request_dict = task_comment_request_instance.to_dict()
# create an instance of TaskCommentRequest from a dict
task_comment_request_from_dict = TaskCommentRequest.from_dict(task_comment_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


