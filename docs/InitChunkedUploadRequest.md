# InitChunkedUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_name** | **str** |  | 
**total_size** | **int** |  | 
**mime_type** | **str** |  | 
**expected_blocks** | **List[str]** | Hashes of every block the client intends to upload. | 
**folder_id** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.init_chunked_upload_request import InitChunkedUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InitChunkedUploadRequest from a JSON string
init_chunked_upload_request_instance = InitChunkedUploadRequest.from_json(json)
# print the JSON string representation of the object
print(InitChunkedUploadRequest.to_json())

# convert the object into a dict
init_chunked_upload_request_dict = init_chunked_upload_request_instance.to_dict()
# create an instance of InitChunkedUploadRequest from a dict
init_chunked_upload_request_from_dict = InitChunkedUploadRequest.from_dict(init_chunked_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


