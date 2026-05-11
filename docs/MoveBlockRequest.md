# MoveBlockRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**parent_id** | **str** | New parent block id; omit to keep the current parent. | [optional] 
**position** | **int** |  | 

## Example

```python
from spatio.models.move_block_request import MoveBlockRequest

# TODO update the JSON string below
json = "{}"
# create an instance of MoveBlockRequest from a JSON string
move_block_request_instance = MoveBlockRequest.from_json(json)
# print the JSON string representation of the object
print(MoveBlockRequest.to_json())

# convert the object into a dict
move_block_request_dict = move_block_request_instance.to_dict()
# create an instance of MoveBlockRequest from a dict
move_block_request_from_dict = MoveBlockRequest.from_dict(move_block_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


