# MeetingRoom


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.meeting_room import MeetingRoom

# TODO update the JSON string below
json = "{}"
# create an instance of MeetingRoom from a JSON string
meeting_room_instance = MeetingRoom.from_json(json)
# print the JSON string representation of the object
print(MeetingRoom.to_json())

# convert the object into a dict
meeting_room_dict = meeting_room_instance.to_dict()
# create an instance of MeetingRoom from a dict
meeting_room_from_dict = MeetingRoom.from_dict(meeting_room_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


