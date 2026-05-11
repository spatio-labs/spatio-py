# BulkDeleteEmailsRequest

Soft-deletes by default (moves to provider trash). Set `permanent: true` to hard-delete. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**message_ids** | **List[str]** |  | 
**permanent** | **bool** |  | [optional] 

## Example

```python
from spatio.models.bulk_delete_emails_request import BulkDeleteEmailsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkDeleteEmailsRequest from a JSON string
bulk_delete_emails_request_instance = BulkDeleteEmailsRequest.from_json(json)
# print the JSON string representation of the object
print(BulkDeleteEmailsRequest.to_json())

# convert the object into a dict
bulk_delete_emails_request_dict = bulk_delete_emails_request_instance.to_dict()
# create an instance of BulkDeleteEmailsRequest from a dict
bulk_delete_emails_request_from_dict = BulkDeleteEmailsRequest.from_dict(bulk_delete_emails_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


