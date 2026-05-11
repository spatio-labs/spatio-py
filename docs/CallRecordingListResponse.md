# CallRecordingListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**recordings** | [**List[CallRecording]**](CallRecording.md) |  | 

## Example

```python
from spatio.models.call_recording_list_response import CallRecordingListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CallRecordingListResponse from a JSON string
call_recording_list_response_instance = CallRecordingListResponse.from_json(json)
# print the JSON string representation of the object
print(CallRecordingListResponse.to_json())

# convert the object into a dict
call_recording_list_response_dict = call_recording_list_response_instance.to_dict()
# create an instance of CallRecordingListResponse from a dict
call_recording_list_response_from_dict = CallRecordingListResponse.from_dict(call_recording_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


