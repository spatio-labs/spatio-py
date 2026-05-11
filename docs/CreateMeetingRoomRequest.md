# CreateMeetingRoomRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**workspace_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_meeting_room_request import CreateMeetingRoomRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateMeetingRoomRequest from a JSON string
create_meeting_room_request_instance = CreateMeetingRoomRequest.from_json(json)
# print the JSON string representation of the object
print(CreateMeetingRoomRequest.to_json())

# convert the object into a dict
create_meeting_room_request_dict = create_meeting_room_request_instance.to_dict()
# create an instance of CreateMeetingRoomRequest from a dict
create_meeting_room_request_from_dict = CreateMeetingRoomRequest.from_dict(create_meeting_room_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


