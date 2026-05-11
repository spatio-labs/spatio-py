# CreateChannelRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**is_private** | **bool** |  | [optional] 

## Example

```python
from spatio.models.create_channel_request import CreateChannelRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateChannelRequest from a JSON string
create_channel_request_instance = CreateChannelRequest.from_json(json)
# print the JSON string representation of the object
print(CreateChannelRequest.to_json())

# convert the object into a dict
create_channel_request_dict = create_channel_request_instance.to_dict()
# create an instance of CreateChannelRequest from a dict
create_channel_request_from_dict = CreateChannelRequest.from_dict(create_channel_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


