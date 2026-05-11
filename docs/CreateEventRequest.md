# CreateEventRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**calendar_id** | **str** | Specific calendar within the account; omit for the default. | [optional] 
**event** | [**SpatioEvent**](SpatioEvent.md) |  | 
**send_updates** | **str** | Notification policy passed through to the provider. | [optional] 
**conference_type** | **str** | When set, the platform will auto-attach a conference link of the matching type (&#x60;spatio&#x60;, &#x60;meet&#x60;, &#x60;zoom&#x60;, &#x60;teams&#x60;).  | [optional] 

## Example

```python
from spatio.models.create_event_request import CreateEventRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateEventRequest from a JSON string
create_event_request_instance = CreateEventRequest.from_json(json)
# print the JSON string representation of the object
print(CreateEventRequest.to_json())

# convert the object into a dict
create_event_request_dict = create_event_request_instance.to_dict()
# create an instance of CreateEventRequest from a dict
create_event_request_from_dict = CreateEventRequest.from_dict(create_event_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


