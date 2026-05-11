# DMThreadReplyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_thread_reply_request import DMThreadReplyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMThreadReplyRequest from a JSON string
dm_thread_reply_request_instance = DMThreadReplyRequest.from_json(json)
# print the JSON string representation of the object
print(DMThreadReplyRequest.to_json())

# convert the object into a dict
dm_thread_reply_request_dict = dm_thread_reply_request_instance.to_dict()
# create an instance of DMThreadReplyRequest from a dict
dm_thread_reply_request_from_dict = DMThreadReplyRequest.from_dict(dm_thread_reply_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


