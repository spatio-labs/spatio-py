# BulkMarkReadResponse

Partial-success envelope for `bulkMarkEmailsRead`. `updated` is a count (not an array — distinct from archive/delete which return the actual id list). The failed-row shape uses `id` (also distinct — renderer-compat legacy). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**updated** | **int** | Number of messages successfully marked. | 
**failed** | [**List[BulkMarkReadResponseFailedInner]**](BulkMarkReadResponseFailedInner.md) |  | 

## Example

```python
from spatio.models.bulk_mark_read_response import BulkMarkReadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of BulkMarkReadResponse from a JSON string
bulk_mark_read_response_instance = BulkMarkReadResponse.from_json(json)
# print the JSON string representation of the object
print(BulkMarkReadResponse.to_json())

# convert the object into a dict
bulk_mark_read_response_dict = bulk_mark_read_response_instance.to_dict()
# create an instance of BulkMarkReadResponse from a dict
bulk_mark_read_response_from_dict = BulkMarkReadResponse.from_dict(bulk_mark_read_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


