# CreateCalendarEvent201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | [**SpatioEvent**](SpatioEvent.md) |  | [optional] 
**errors** | [**List[CalendarAccountError]**](CalendarAccountError.md) |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_calendar_event201_response import CreateCalendarEvent201Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCalendarEvent201Response from a JSON string
create_calendar_event201_response_instance = CreateCalendarEvent201Response.from_json(json)
# print the JSON string representation of the object
print(CreateCalendarEvent201Response.to_json())

# convert the object into a dict
create_calendar_event201_response_dict = create_calendar_event201_response_instance.to_dict()
# create an instance of CreateCalendarEvent201Response from a dict
create_calendar_event201_response_from_dict = CreateCalendarEvent201Response.from_dict(create_calendar_event201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


