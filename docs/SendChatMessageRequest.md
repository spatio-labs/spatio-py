# SendChatMessageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**channel** | **str** | Channel or DM id (provider-scoped). | 
**text** | **str** |  | 
**thread_id** | **str** |  | [optional] 
**blocks** | **List[Dict[str, object]]** | Provider-specific rich-message blocks. | [optional] 

## Example

```python
from spatio.models.send_chat_message_request import SendChatMessageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SendChatMessageRequest from a JSON string
send_chat_message_request_instance = SendChatMessageRequest.from_json(json)
# print the JSON string representation of the object
print(SendChatMessageRequest.to_json())

# convert the object into a dict
send_chat_message_request_dict = send_chat_message_request_instance.to_dict()
# create an instance of SendChatMessageRequest from a dict
send_chat_message_request_from_dict = SendChatMessageRequest.from_dict(send_chat_message_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


