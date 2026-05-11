# BulkFilesResponseFailedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**file_id** | **str** |  | 
**error** | **str** |  | 

## Example

```python
from spatio.models.bulk_files_response_failed_inner import BulkFilesResponseFailedInner

# TODO update the JSON string below
json = "{}"
# create an instance of BulkFilesResponseFailedInner from a JSON string
bulk_files_response_failed_inner_instance = BulkFilesResponseFailedInner.from_json(json)
# print the JSON string representation of the object
print(BulkFilesResponseFailedInner.to_json())

# convert the object into a dict
bulk_files_response_failed_inner_dict = bulk_files_response_failed_inner_instance.to_dict()
# create an instance of BulkFilesResponseFailedInner from a dict
bulk_files_response_failed_inner_from_dict = BulkFilesResponseFailedInner.from_dict(bulk_files_response_failed_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


