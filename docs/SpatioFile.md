# SpatioFile

A user file. Files belong to one connected file provider account (`accountId` + `provider`); native storage uses Spatio's block-store, external providers (Google Drive, Dropbox, etc.) round-trip through Spatio.  Schema name is `SpatioFile` (not `File`) to avoid the `java.io.File` collision that breaks the Kotlin SDK generator when the schema is named `File`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**size** | **int** | Bytes. | 
**mime_type** | **str** |  | 
**folder_id** | **str** |  | [optional] 
**storage_type** | **str** | Backing storage class — &#x60;r2&#x60;, &#x60;gdrive&#x60;, &#x60;dropbox&#x60;, etc. Provider-specific; treat as opaque.  | 
**download_url** | **str** | Pre-signed download URL when one is cached on the row. Use &#x60;GET /v1/files/{id}/download&#x60; for a guaranteed-fresh URL — this field can lag past expiry.  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.spatio_file import SpatioFile

# TODO update the JSON string below
json = "{}"
# create an instance of SpatioFile from a JSON string
spatio_file_instance = SpatioFile.from_json(json)
# print the JSON string representation of the object
print(SpatioFile.to_json())

# convert the object into a dict
spatio_file_dict = spatio_file_instance.to_dict()
# create an instance of SpatioFile from a dict
spatio_file_from_dict = SpatioFile.from_dict(spatio_file_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


