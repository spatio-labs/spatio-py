# Comment

Threaded comment on a note. Top-level comments have `parentCommentId: null`; replies set it to the parent comment's id. `blockId` anchors the comment to a specific block; comments without a `blockId` are note-level (\"general\") comments. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**note_id** | **str** |  | 
**parent_comment_id** | **str** |  | [optional] 
**block_id** | **str** |  | [optional] 
**body** | **str** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**author** | [**CommentAuthor**](CommentAuthor.md) |  | 

## Example

```python
from spatio.models.comment import Comment

# TODO update the JSON string below
json = "{}"
# create an instance of Comment from a JSON string
comment_instance = Comment.from_json(json)
# print the JSON string representation of the object
print(Comment.to_json())

# convert the object into a dict
comment_dict = comment_instance.to_dict()
# create an instance of Comment from a dict
comment_from_dict = Comment.from_dict(comment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


