# UpdateParticipantStateRequest

Toggle audio/video/screen-share state.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**audio_enabled** | **bool** |  | [optional] 
**video_enabled** | **bool** |  | [optional] 
**screen_share_enabled** | **bool** |  | [optional] 

## Example

```python
from spatio.models.update_participant_state_request import UpdateParticipantStateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateParticipantStateRequest from a JSON string
update_participant_state_request_instance = UpdateParticipantStateRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateParticipantStateRequest.to_json())

# convert the object into a dict
update_participant_state_request_dict = update_participant_state_request_instance.to_dict()
# create an instance of UpdateParticipantStateRequest from a dict
update_participant_state_request_from_dict = UpdateParticipantStateRequest.from_dict(update_participant_state_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


