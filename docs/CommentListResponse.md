# CommentListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**comments** | [**List[Comment]**](Comment.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.comment_list_response import CommentListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CommentListResponse from a JSON string
comment_list_response_instance = CommentListResponse.from_json(json)
# print the JSON string representation of the object
print(CommentListResponse.to_json())

# convert the object into a dict
comment_list_response_dict = comment_list_response_instance.to_dict()
# create an instance of CommentListResponse from a dict
comment_list_response_from_dict = CommentListResponse.from_dict(comment_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


