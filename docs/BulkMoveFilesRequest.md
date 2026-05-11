# BulkMoveFilesRequest

Move multiple files to one target folder. `targetFolderId` is the canonical name; `folderId` is accepted as a renderer-compat alias. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_ids** | **List[str]** |  | [optional] 
**account_ids** | **List[str]** |  | [optional] 
**account_id** | **str** |  | [optional] 
**target_folder_id** | **str** |  | [optional] 
**folder_id** | **str** | Alias for &#x60;targetFolderId&#x60;. | [optional] 

## Example

```python
from spatio.models.bulk_move_files_request import BulkMoveFilesRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkMoveFilesRequest from a JSON string
bulk_move_files_request_instance = BulkMoveFilesRequest.from_json(json)
# print the JSON string representation of the object
print(BulkMoveFilesRequest.to_json())

# convert the object into a dict
bulk_move_files_request_dict = bulk_move_files_request_instance.to_dict()
# create an instance of BulkMoveFilesRequest from a dict
bulk_move_files_request_from_dict = BulkMoveFilesRequest.from_dict(bulk_move_files_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


