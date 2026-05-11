# ChatMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**channel_id** | **str** |  | 
**user_id** | **str** |  | 
**text** | **str** |  | 
**thread_id** | **str** | Set on replies and on parent messages once a thread exists.  | [optional] 
**timestamp** | **datetime** |  | 
**reply_count** | **int** |  | [optional] 
**extra** | **Dict[str, object]** | Provider-specific extras. | [optional] 

## Example

```python
from spatio.models.chat_message import ChatMessage

# TODO update the JSON string below
json = "{}"
# create an instance of ChatMessage from a JSON string
chat_message_instance = ChatMessage.from_json(json)
# print the JSON string representation of the object
print(ChatMessage.to_json())

# convert the object into a dict
chat_message_dict = chat_message_instance.to_dict()
# create an instance of ChatMessage from a dict
chat_message_from_dict = ChatMessage.from_dict(chat_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


