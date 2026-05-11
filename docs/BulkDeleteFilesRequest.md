# BulkDeleteFilesRequest

Either `fileIds` (with optional parallel `accountIds`) for multi-file delete, or `fileId` (with optional `accountId`) for the single-file fallback. `fileIds` wins when both are set. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_ids** | **List[str]** |  | [optional] 
**account_ids** | **List[str]** | Parallel slice with fileIds — accountIds[i] targets fileIds[i]. | [optional] 
**file_id** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.bulk_delete_files_request import BulkDeleteFilesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteFilesRequest from a JSON string
bulk_delete_files_request_instance = BulkDeleteFilesRequest.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteFilesRequest.to_json())

# convert the object into a dict
bulk_delete_files_request_dict = bulk_delete_files_request_instance.to_dict()
# create an instance of BulkDeleteFilesRequest from a dict
bulk_delete_files_request_from_dict = BulkDeleteFilesRequest.from_dict(bulk_delete_files_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


