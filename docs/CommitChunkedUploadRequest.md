# CommitChunkedUploadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**session_id** | **str** |  | 

## Example

```python
from spatio.models.commit_chunked_upload_request import CommitChunkedUploadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CommitChunkedUploadRequest from a JSON string
commit_chunked_upload_request_instance = CommitChunkedUploadRequest.from_json(json)
# print the JSON string representation of the object
print(CommitChunkedUploadRequest.to_json())

# convert the object into a dict
commit_chunked_upload_request_dict = commit_chunked_upload_request_instance.to_dict()
# create an instance of CommitChunkedUploadRequest from a dict
commit_chunked_upload_request_from_dict = CommitChunkedUploadRequest.from_dict(commit_chunked_upload_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


