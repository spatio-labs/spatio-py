# CommentMutationResponse

Response for `POST` and `PATCH` on a comment.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comment** | [**Comment**](Comment.md) |  | 
**success** | **bool** |  | 

## Example

```python
from spatio.models.comment_mutation_response import CommentMutationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CommentMutationResponse from a JSON string
comment_mutation_response_instance = CommentMutationResponse.from_json(json)
# print the JSON string representation of the object
print(CommentMutationResponse.to_json())

# convert the object into a dict
comment_mutation_response_dict = comment_mutation_response_instance.to_dict()
# create an instance of CommentMutationResponse from a dict
comment_mutation_response_from_dict = CommentMutationResponse.from_dict(comment_mutation_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


