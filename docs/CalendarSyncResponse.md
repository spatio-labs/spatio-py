# CalendarSyncResponse

Returned by `POST /v1/calendar/sync`. Status code is `202` by default (sync jobs queued); `200` when called with `?wait=true` and all jobs finish within the 10-second polling budget. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enqueued** | **int** |  | 
**jobs** | **List[str]** |  | 
**waited** | **bool** |  | [optional] 
**timed_out** | **bool** |  | [optional] 
**errors** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.calendar_sync_response import CalendarSyncResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarSyncResponse from a JSON string
calendar_sync_response_instance = CalendarSyncResponse.from_json(json)
# print the JSON string representation of the object
print(CalendarSyncResponse.to_json())

# convert the object into a dict
calendar_sync_response_dict = calendar_sync_response_instance.to_dict()
# create an instance of CalendarSyncResponse from a dict
calendar_sync_response_from_dict = CalendarSyncResponse.from_dict(calendar_sync_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


