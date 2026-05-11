# SpatioEvent

A calendar event. Calendar uses snake_case JSON keys (different from Notes/Sheets/Slides/Tasks/Mail which use camelCase) — the surface predates the cross-platform convention. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**start_time** | **datetime** |  | 
**end_time** | **datetime** |  | 
**all_day** | **bool** |  | 
**location** | **str** |  | [optional] 
**location_details** | **Dict[str, str]** | Free-form key/value (lat, lng, room, etc.). | [optional] 
**organizer** | **str** | Organizer email. | [optional] 
**attendees** | [**List[Attendee]**](Attendee.md) |  | [optional] 
**recurrence_rule** | **str** | RFC 5545 RRULE. | [optional] 
**recurrence_id** | **str** | Set on instances of a recurring series. | [optional] 
**original_start** | **datetime** | Original start of a moved recurring instance. | [optional] 
**status** | **str** | Provider-mapped event status. Free-form string — common values are &#x60;confirmed&#x60;, &#x60;tentative&#x60;, &#x60;cancelled&#x60;, &#x60;needs_action&#x60;, and the empty string when the provider doesn&#39;t populate it. Not enumerated strictly because providers add custom values and the platform passes them through verbatim.  | 
**visibility** | **str** | Free-form visibility string. Common values: &#x60;public&#x60;, &#x60;private&#x60;, &#x60;confidential&#x60;, plus empty when unset.  | 
**busy** | **bool** | Whether this event marks the time as busy or free. | 
**reminders** | [**List[Reminder]**](Reminder.md) |  | [optional] 
**travel_time_minutes** | **int** | Apple Calendar&#39;s local-only travel buffer. Stored on the cached row but not synced to providers that don&#39;t model it.  | [optional] 
**categories** | **List[str]** |  | [optional] 
**color** | **str** |  | [optional] 
**user_id** | **str** |  | [optional] 
**account_id** | **str** |  | 
**provider** | **str** | Standardized provider id (e.g. &#x60;google-calendar&#x60;, &#x60;native-calendar&#x60;). Mirrors &#x60;provider_id&#x60; — both are populated on writes; clients should prefer &#x60;provider&#x60;.  | [optional] 
**provider_id** | **str** | Legacy alias of &#x60;provider&#x60;. | 
**provider_data** | **Dict[str, object]** | Provider-specific extras. | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**deleted_at** | **datetime** |  | [optional] 
**synced_at** | **datetime** |  | [optional] 
**conference_data** | [**ConferenceData**](ConferenceData.md) |  | [optional] 
**attachments** | [**List[Attachment]**](Attachment.md) |  | [optional] 
**url** | **str** |  | [optional] 
**etag** | **str** |  | [optional] 
**sequence** | **int** |  | [optional] 
**custom_data** | **Dict[str, str]** |  | [optional] 

## Example

```python
from spatio.models.spatio_event import SpatioEvent

# TODO update the JSON string below
json = "{}"
# create an instance of SpatioEvent from a JSON string
spatio_event_instance = SpatioEvent.from_json(json)
# print the JSON string representation of the object
print(SpatioEvent.to_json())

# convert the object into a dict
spatio_event_dict = spatio_event_instance.to_dict()
# create an instance of SpatioEvent from a dict
spatio_event_from_dict = SpatioEvent.from_dict(spatio_event_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


