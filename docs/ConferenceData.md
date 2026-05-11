# ConferenceData

Video/phone conference details. `type` is canonical (`spatio`, `meet`, `zoom`, `teams`); other provider-specific values are accepted as opaque strings. The Spatio invite email pipeline only fires for native events or events with `type: spatio`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**uri** | **str** |  | 
**meeting_id** | **str** |  | [optional] 
**passcode** | **str** |  | [optional] 
**access_code** | **str** |  | [optional] 
**dial_in** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.conference_data import ConferenceData

# TODO update the JSON string below
json = "{}"
# create an instance of ConferenceData from a JSON string
conference_data_instance = ConferenceData.from_json(json)
# print the JSON string representation of the object
print(ConferenceData.to_json())

# convert the object into a dict
conference_data_dict = conference_data_instance.to_dict()
# create an instance of ConferenceData from a dict
conference_data_from_dict = ConferenceData.from_dict(conference_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


