# DMMarkReadRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_id** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_mark_read_request import DMMarkReadRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMMarkReadRequest from a JSON string
dm_mark_read_request_instance = DMMarkReadRequest.from_json(json)
# print the JSON string representation of the object
print(DMMarkReadRequest.to_json())

# convert the object into a dict
dm_mark_read_request_dict = dm_mark_read_request_instance.to_dict()
# create an instance of DMMarkReadRequest from a dict
dm_mark_read_request_from_dict = DMMarkReadRequest.from_dict(dm_mark_read_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


