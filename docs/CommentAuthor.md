# CommentAuthor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**email** | **str** |  | 
**profile_photo** | **str** |  | [optional] 

## Example

```python
from spatio.models.comment_author import CommentAuthor

# TODO update the JSON string below
json = "{}"
# create an instance of CommentAuthor from a JSON string
comment_author_instance = CommentAuthor.from_json(json)
# print the JSON string representation of the object
print(CommentAuthor.to_json())

# convert the object into a dict
comment_author_dict = comment_author_instance.to_dict()
# create an instance of CommentAuthor from a dict
comment_author_from_dict = CommentAuthor.from_dict(comment_author_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


