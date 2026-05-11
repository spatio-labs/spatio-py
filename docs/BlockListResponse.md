# BlockListResponse

Single-account list response for `GET /v1/notes/{id}/blocks`. Unlike `GET /v1/notes`, block listing always targets one account so it does not fan out — `total` is the count for the current page slice. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**blocks** | [**List[Block]**](Block.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.block_list_response import BlockListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BlockListResponse from a JSON string
block_list_response_instance = BlockListResponse.from_json(json)
# print the JSON string representation of the object
print(BlockListResponse.to_json())

# convert the object into a dict
block_list_response_dict = block_list_response_instance.to_dict()
# create an instance of BlockListResponse from a dict
block_list_response_from_dict = BlockListResponse.from_dict(block_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


