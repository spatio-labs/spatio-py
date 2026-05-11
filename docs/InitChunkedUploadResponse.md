# InitChunkedUploadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | 
**blocks_to_upload** | **List[str]** |  | 
**blocks_already_exist** | **List[str]** | Blocks the platform already has and the client can skip (content-addressed deduplication).  | 
**deduplication_pct** | **float** |  | 
**estimated_upload_size** | **int** |  | 

## Example

```python
from spatio.models.init_chunked_upload_response import InitChunkedUploadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of InitChunkedUploadResponse from a JSON string
init_chunked_upload_response_instance = InitChunkedUploadResponse.from_json(json)
# print the JSON string representation of the object
print(InitChunkedUploadResponse.to_json())

# convert the object into a dict
init_chunked_upload_response_dict = init_chunked_upload_response_instance.to_dict()
# create an instance of InitChunkedUploadResponse from a dict
init_chunked_upload_response_from_dict = InitChunkedUploadResponse.from_dict(init_chunked_upload_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


