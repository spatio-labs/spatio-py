# CommitChunkedUploadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**file_id** | **str** |  | 
**manifest_id** | **str** |  | 
**version** | **int** |  | 
**total_size** | **int** |  | 
**physical_size** | **int** |  | [optional] 
**deduplication_pct** | **float** |  | [optional] 
**total_blocks** | **int** |  | [optional] 
**new_blocks** | **int** |  | [optional] 
**deduplicated_blocks** | **int** |  | [optional] 

## Example

```python
from spatio.models.commit_chunked_upload_response import CommitChunkedUploadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CommitChunkedUploadResponse from a JSON string
commit_chunked_upload_response_instance = CommitChunkedUploadResponse.from_json(json)
# print the JSON string representation of the object
print(CommitChunkedUploadResponse.to_json())

# convert the object into a dict
commit_chunked_upload_response_dict = commit_chunked_upload_response_instance.to_dict()
# create an instance of CommitChunkedUploadResponse from a dict
commit_chunked_upload_response_from_dict = CommitChunkedUploadResponse.from_dict(commit_chunked_upload_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


