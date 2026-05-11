# ListChannelsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channels** | [**List[Channel]**](Channel.md) | &#x60;null&#x60; when no results (Go nil-slice serialization). | [optional] 
**total** | **int** |  | 
**next_cursor** | **str** |  | [optional] 
**provider** | **str** |  | 

## Example

```python
from spatio.models.list_channels_response import ListChannelsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListChannelsResponse from a JSON string
list_channels_response_instance = ListChannelsResponse.from_json(json)
# print the JSON string representation of the object
print(ListChannelsResponse.to_json())

# convert the object into a dict
list_channels_response_dict = list_channels_response_instance.to_dict()
# create an instance of ListChannelsResponse from a dict
list_channels_response_from_dict = ListChannelsResponse.from_dict(list_channels_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


