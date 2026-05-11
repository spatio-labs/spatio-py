# BulkArchiveRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**message_ids** | **List[str]** |  | 

## Example

```python
from spatio.models.bulk_archive_request import BulkArchiveRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkArchiveRequest from a JSON string
bulk_archive_request_instance = BulkArchiveRequest.from_json(json)
# print the JSON string representation of the object
print(BulkArchiveRequest.to_json())

# convert the object into a dict
bulk_archive_request_dict = bulk_archive_request_instance.to_dict()
# create an instance of BulkArchiveRequest from a dict
bulk_archive_request_from_dict = BulkArchiveRequest.from_dict(bulk_archive_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


