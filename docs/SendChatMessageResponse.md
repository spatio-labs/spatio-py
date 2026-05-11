# SendChatMessageResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**message_id** | **str** |  | 
**channel_id** | **str** |  | [optional] 
**thread_id** | **str** |  | [optional] 
**provider** | **str** |  | 
**error** | **str** |  | [optional] 

## Example

```python
from spatio.models.send_chat_message_response import SendChatMessageResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SendChatMessageResponse from a JSON string
send_chat_message_response_instance = SendChatMessageResponse.from_json(json)
# print the JSON string representation of the object
print(SendChatMessageResponse.to_json())

# convert the object into a dict
send_chat_message_response_dict = send_chat_message_response_instance.to_dict()
# create an instance of SendChatMessageResponse from a dict
send_chat_message_response_from_dict = SendChatMessageResponse.from_dict(send_chat_message_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


