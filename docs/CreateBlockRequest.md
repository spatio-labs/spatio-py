# CreateBlockRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**BlockType**](BlockType.md) |  | 
**content** | [**BlockContent**](BlockContent.md) |  | 
**parent_id** | **str** | Parent block id for nested blocks. | [optional] 
**position** | **int** |  | 
**properties** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_block_request import CreateBlockRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateBlockRequest from a JSON string
create_block_request_instance = CreateBlockRequest.from_json(json)
# print the JSON string representation of the object
print(CreateBlockRequest.to_json())

# convert the object into a dict
create_block_request_dict = create_block_request_instance.to_dict()
# create an instance of CreateBlockRequest from a dict
create_block_request_from_dict = CreateBlockRequest.from_dict(create_block_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


