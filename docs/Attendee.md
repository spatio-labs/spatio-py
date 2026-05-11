# Attendee


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | **str** |  | 
**name** | **str** |  | [optional] 
**status** | [**AttendeeStatus**](AttendeeStatus.md) |  | 
**role** | [**AttendeeRole**](AttendeeRole.md) |  | 
**optional** | **bool** | Legacy boolean — superseded by &#x60;role&#x60; (&#x60;role: optional&#x60; carries the same signal). Kept on the wire for client compatibility.  | 
**comment** | **str** |  | [optional] 
**additional_guests** | **int** |  | [optional] 

## Example

```python
from spatio.models.attendee import Attendee

# TODO update the JSON string below
json = "{}"
# create an instance of Attendee from a JSON string
attendee_instance = Attendee.from_json(json)
# print the JSON string representation of the object
print(Attendee.to_json())

# convert the object into a dict
attendee_dict = attendee_instance.to_dict()
# create an instance of Attendee from a dict
attendee_from_dict = Attendee.from_dict(attendee_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


