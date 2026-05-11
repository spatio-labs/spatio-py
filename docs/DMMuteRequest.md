# DMMuteRequest

Mute either until a specific time (`untilSeconds`, Unix epoch) or forever (`forever: true`). At least one must be set. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**until_seconds** | **int** |  | [optional] 
**forever** | **bool** |  | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_mute_request import DMMuteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMMuteRequest from a JSON string
dm_mute_request_instance = DMMuteRequest.from_json(json)
# print the JSON string representation of the object
print(DMMuteRequest.to_json())

# convert the object into a dict
dm_mute_request_dict = dm_mute_request_instance.to_dict()
# create an instance of DMMuteRequest from a dict
dm_mute_request_from_dict = DMMuteRequest.from_dict(dm_mute_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


