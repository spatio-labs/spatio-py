# BulkDeleteEmailsResponse

Partial-success envelope for `bulkDeleteEmails`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**deleted** | **List[str]** |  | 
**failed** | [**List[BulkArchiveResponseFailedInner]**](BulkArchiveResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_delete_emails_response import BulkDeleteEmailsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteEmailsResponse from a JSON string
bulk_delete_emails_response_instance = BulkDeleteEmailsResponse.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteEmailsResponse.to_json())

# convert the object into a dict
bulk_delete_emails_response_dict = bulk_delete_emails_response_instance.to_dict()
# create an instance of BulkDeleteEmailsResponse from a dict
bulk_delete_emails_response_from_dict = BulkDeleteEmailsResponse.from_dict(bulk_delete_emails_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


