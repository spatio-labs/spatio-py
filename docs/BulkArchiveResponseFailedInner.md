# BulkArchiveResponseFailedInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | **str** |  | 
**error** | **str** |  | 

## Example

```python
from spatio.models.bulk_archive_response_failed_inner import BulkArchiveResponseFailedInner

# TODO update the JSON string below
json = "{}"
# create an instance of BulkArchiveResponseFailedInner from a JSON string
bulk_archive_response_failed_inner_instance = BulkArchiveResponseFailedInner.from_json(json)
# print the JSON string representation of the object
print(BulkArchiveResponseFailedInner.to_json())

# convert the object into a dict
bulk_archive_response_failed_inner_dict = bulk_archive_response_failed_inner_instance.to_dict()
# create an instance of BulkArchiveResponseFailedInner from a dict
bulk_archive_response_failed_inner_from_dict = BulkArchiveResponseFailedInner.from_dict(bulk_archive_response_failed_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


