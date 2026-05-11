# DMForwardRequest

Forward to either a DM (`toDmId`) or a channel (`toChannelId`); exactly one required.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**to_dm_id** | **str** |  | [optional] 
**to_channel_id** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_forward_request import DMForwardRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMForwardRequest from a JSON string
dm_forward_request_instance = DMForwardRequest.from_json(json)
# print the JSON string representation of the object
print(DMForwardRequest.to_json())

# convert the object into a dict
dm_forward_request_dict = dm_forward_request_instance.to_dict()
# create an instance of DMForwardRequest from a dict
dm_forward_request_from_dict = DMForwardRequest.from_dict(dm_forward_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


