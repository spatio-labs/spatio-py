# CreateChannelResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | [**Channel**](Channel.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.create_channel_response import CreateChannelResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreateChannelResponse from a JSON string
create_channel_response_instance = CreateChannelResponse.from_json(json)
# print the JSON string representation of the object
print(CreateChannelResponse.to_json())

# convert the object into a dict
create_channel_response_dict = create_channel_response_instance.to_dict()
# create an instance of CreateChannelResponse from a dict
create_channel_response_from_dict = CreateChannelResponse.from_dict(create_channel_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


