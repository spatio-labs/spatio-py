# UpdateEventRequest

Sparse update. `updates` is a free-form map of fields to change; only keys present are applied. The server-side capability gate rejects fields that the underlying provider doesn't support. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**updates** | **Dict[str, object]** |  | 
**send_updates** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_event_request import UpdateEventRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEventRequest from a JSON string
update_event_request_instance = UpdateEventRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateEventRequest.to_json())

# convert the object into a dict
update_event_request_dict = update_event_request_instance.to_dict()
# create an instance of UpdateEventRequest from a dict
update_event_request_from_dict = UpdateEventRequest.from_dict(update_event_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


