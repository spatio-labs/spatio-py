# FilesAndFoldersResponse

Aggregated `{files, folders, accounts}` envelope used by the renderer's file-browser. Calls `ListFiles` and `ListFolders` in parallel and merges the results — saves a round-trip when the UI shows both side-by-side. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**files** | [**List[SpatioFile]**](SpatioFile.md) |  | [optional] 
**folders** | [**List[Folder]**](Folder.md) |  | [optional] 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | [optional] 
**total** | **int** |  | 
**has_more** | **bool** |  | 
**next_offset** | **int** |  | [optional] 

## Example

```python
from spatio.models.files_and_folders_response import FilesAndFoldersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of FilesAndFoldersResponse from a JSON string
files_and_folders_response_instance = FilesAndFoldersResponse.from_json(json)
# print the JSON string representation of the object
print(FilesAndFoldersResponse.to_json())

# convert the object into a dict
files_and_folders_response_dict = files_and_folders_response_instance.to_dict()
# create an instance of FilesAndFoldersResponse from a dict
files_and_folders_response_from_dict = FilesAndFoldersResponse.from_dict(files_and_folders_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


