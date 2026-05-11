# TaskCommentMutationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comment** | [**TaskComment**](TaskComment.md) |  | 
**success** | **bool** |  | 

## Example

```python
from spatio.models.task_comment_mutation_response import TaskCommentMutationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TaskCommentMutationResponse from a JSON string
task_comment_mutation_response_instance = TaskCommentMutationResponse.from_json(json)
# print the JSON string representation of the object
print(TaskCommentMutationResponse.to_json())

# convert the object into a dict
task_comment_mutation_response_dict = task_comment_mutation_response_instance.to_dict()
# create an instance of TaskCommentMutationResponse from a dict
task_comment_mutation_response_from_dict = TaskCommentMutationResponse.from_dict(task_comment_mutation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


