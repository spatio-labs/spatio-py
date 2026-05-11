# ChunkedFileManifest

Block-level manifest for a chunked-uploaded file. Returned by `GET /v1/files/{id}/manifest`. Only meaningful for files uploaded via the chunked path; legacy uploads return `404`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**manifest_id** | **str** |  | 
**file_id** | **str** |  | 
**file_name** | **str** |  | 
**version** | **int** |  | 
**total_size** | **int** |  | 
**block_count** | **int** |  | 
**chunking_algorithm** | **str** |  | [optional] 
**file_checksum** | **str** |  | [optional] 
**blocks** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.chunked_file_manifest import ChunkedFileManifest

# TODO update the JSON string below
json = "{}"
# create an instance of ChunkedFileManifest from a JSON string
chunked_file_manifest_instance = ChunkedFileManifest.from_json(json)
# print the JSON string representation of the object
print(ChunkedFileManifest.to_json())

# convert the object into a dict
chunked_file_manifest_dict = chunked_file_manifest_instance.to_dict()
# create an instance of ChunkedFileManifest from a dict
chunked_file_manifest_from_dict = ChunkedFileManifest.from_dict(chunked_file_manifest_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


