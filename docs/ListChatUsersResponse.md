# ListChatUsersResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**users** | [**List[ChatUser]**](ChatUser.md) |  | [optional] 
**total** | **int** |  | 
**next_cursor** | **str** |  | [optional] 
**provider** | **str** |  | 

## Example

```python
from spatio.models.list_chat_users_response import ListChatUsersResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ListChatUsersResponse from a JSON string
list_chat_users_response_instance = ListChatUsersResponse.from_json(json)
# print the JSON string representation of the object
print(ListChatUsersResponse.to_json())

# convert the object into a dict
list_chat_users_response_dict = list_chat_users_response_instance.to_dict()
# create an instance of ListChatUsersResponse from a dict
list_chat_users_response_from_dict = ListChatUsersResponse.from_dict(list_chat_users_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


