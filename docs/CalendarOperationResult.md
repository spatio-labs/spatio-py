# CalendarOperationResult

Generic platform-operation envelope used by Calendar list/create/ update/delete responses. `data` is operation-specific:   - listEvents: `ListEventsData`   - createEvent / updateEvent: `Event`   - deleteEvent: empty / metadata-only 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | **object** | Operation-specific payload. See the operation&#39;s response description for the concrete shape.  | [optional] 
**errors** | [**List[CalendarAccountError]**](CalendarAccountError.md) |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.calendar_operation_result import CalendarOperationResult

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarOperationResult from a JSON string
calendar_operation_result_instance = CalendarOperationResult.from_json(json)
# print the JSON string representation of the object
print(CalendarOperationResult.to_json())

# convert the object into a dict
calendar_operation_result_dict = calendar_operation_result_instance.to_dict()
# create an instance of CalendarOperationResult from a dict
calendar_operation_result_from_dict = CalendarOperationResult.from_dict(calendar_operation_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


