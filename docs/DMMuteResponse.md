# DMMuteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**muted_until** | **int** |  | [optional] 

## Example

```python
from spatio.models.dm_mute_response import DMMuteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DMMuteResponse from a JSON string
dm_mute_response_instance = DMMuteResponse.from_json(json)
# print the JSON string representation of the object
print(DMMuteResponse.to_json())

# convert the object into a dict
dm_mute_response_dict = dm_mute_response_instance.to_dict()
# create an instance of DMMuteResponse from a dict
dm_mute_response_from_dict = DMMuteResponse.from_dict(dm_mute_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


