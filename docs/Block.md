# Block


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**note_id** | **str** |  | 
**parent_id** | **str** |  | [optional] 
**type** | [**BlockType**](BlockType.md) |  | 
**content** | [**BlockContent**](BlockContent.md) |  | 
**properties** | **Dict[str, object]** |  | [optional] 
**position** | **int** | Order within the parent (0-indexed). | 
**has_children** | **bool** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.block import Block

# TODO update the JSON string below
json = "{}"
# create an instance of Block from a JSON string
block_instance = Block.from_json(json)
# print the JSON string representation of the object
print(Block.to_json())

# convert the object into a dict
block_dict = block_instance.to_dict()
# create an instance of Block from a dict
block_from_dict = Block.from_dict(block_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


