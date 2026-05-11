# UploadChunkedBlockResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**block_hash** | **str** |  | 
**uploaded** | **bool** |  | 
**blocks_remaining** | **int** |  | 
**progress** | **float** | Percent complete, 0–100. | 

## Example

```python
from spatio.models.upload_chunked_block_response import UploadChunkedBlockResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UploadChunkedBlockResponse from a JSON string
upload_chunked_block_response_instance = UploadChunkedBlockResponse.from_json(json)
# print the JSON string representation of the object
print(UploadChunkedBlockResponse.to_json())

# convert the object into a dict
upload_chunked_block_response_dict = upload_chunked_block_response_instance.to_dict()
# create an instance of UploadChunkedBlockResponse from a dict
upload_chunked_block_response_from_dict = UploadChunkedBlockResponse.from_dict(upload_chunked_block_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


