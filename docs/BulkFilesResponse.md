# BulkFilesResponse

Partial-success envelope for bulk delete/move.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**affected_count** | **int** |  | 
**file_ids** | **List[str]** |  | 
**failed** | [**List[BulkFilesResponseFailedInner]**](BulkFilesResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_files_response import BulkFilesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkFilesResponse from a JSON string
bulk_files_response_instance = BulkFilesResponse.from_json(json)
# print the JSON string representation of the object
print(BulkFilesResponse.to_json())

# convert the object into a dict
bulk_files_response_dict = bulk_files_response_instance.to_dict()
# create an instance of BulkFilesResponse from a dict
bulk_files_response_from_dict = BulkFilesResponse.from_dict(bulk_files_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


