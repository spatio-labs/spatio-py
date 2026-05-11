# CalendarCapabilitiesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**provider_id** | **str** |  | 
**capabilities** | **Dict[str, object]** | Per-account feature gate. The renderer reads these to enable/ disable form fields (recurrence pickers, attendee inputs, etc.) based on what the underlying provider supports.  | 

## Example

```python
from spatio.models.calendar_capabilities_response import CalendarCapabilitiesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarCapabilitiesResponse from a JSON string
calendar_capabilities_response_instance = CalendarCapabilitiesResponse.from_json(json)
# print the JSON string representation of the object
print(CalendarCapabilitiesResponse.to_json())

# convert the object into a dict
calendar_capabilities_response_dict = calendar_capabilities_response_instance.to_dict()
# create an instance of CalendarCapabilitiesResponse from a dict
calendar_capabilities_response_from_dict = CalendarCapabilitiesResponse.from_dict(calendar_capabilities_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


