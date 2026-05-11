# GetChatUserResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | [**ChatUser**](ChatUser.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.get_chat_user_response import GetChatUserResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetChatUserResponse from a JSON string
get_chat_user_response_instance = GetChatUserResponse.from_json(json)
# print the JSON string representation of the object
print(GetChatUserResponse.to_json())

# convert the object into a dict
get_chat_user_response_dict = get_chat_user_response_instance.to_dict()
# create an instance of GetChatUserResponse from a dict
get_chat_user_response_from_dict = GetChatUserResponse.from_dict(get_chat_user_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


