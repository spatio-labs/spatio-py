# BulkMarkReadRequest

Bulk shorthand for setting read state on many messages at once. `messageIds` accepts an array; the production handler also accepts a bare string for renderer-compat but the spec models the array shape only. `read` defaults to `true` when omitted. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**message_ids** | **List[str]** |  | 
**read** | **bool** |  | [optional] [default to True]

## Example

```python
from spatio.models.bulk_mark_read_request import BulkMarkReadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of BulkMarkReadRequest from a JSON string
bulk_mark_read_request_instance = BulkMarkReadRequest.from_json(json)
# print the JSON string representation of the object
print(BulkMarkReadRequest.to_json())

# convert the object into a dict
bulk_mark_read_request_dict = bulk_mark_read_request_instance.to_dict()
# create an instance of BulkMarkReadRequest from a dict
bulk_mark_read_request_from_dict = BulkMarkReadRequest.from_dict(bulk_mark_read_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


