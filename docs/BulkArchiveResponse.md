# BulkArchiveResponse

Partial-success envelope for `bulkArchiveEmails`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** | &#x60;true&#x60; only when zero rows in &#x60;failed&#x60;. | 
**archived** | **List[str]** |  | 
**failed** | [**List[BulkArchiveResponseFailedInner]**](BulkArchiveResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_archive_response import BulkArchiveResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkArchiveResponse from a JSON string
bulk_archive_response_instance = BulkArchiveResponse.from_json(json)
# print the JSON string representation of the object
print(BulkArchiveResponse.to_json())

# convert the object into a dict
bulk_archive_response_dict = bulk_archive_response_instance.to_dict()
# create an instance of BulkArchiveResponse from a dict
bulk_archive_response_from_dict = BulkArchiveResponse.from_dict(bulk_archive_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


