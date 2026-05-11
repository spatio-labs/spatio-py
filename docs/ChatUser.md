# ChatUser


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**real_name** | **str** |  | [optional] 
**email** | **str** |  | [optional] 
**avatar** | **str** |  | [optional] 
**is_bot** | **bool** |  | 
**is_active** | **bool** |  | 

## Example

```python
from spatio.models.chat_user import ChatUser

# TODO update the JSON string below
json = "{}"
# create an instance of ChatUser from a JSON string
chat_user_instance = ChatUser.from_json(json)
# print the JSON string representation of the object
print(ChatUser.to_json())

# convert the object into a dict
chat_user_dict = chat_user_instance.to_dict()
# create an instance of ChatUser from a dict
chat_user_from_dict = ChatUser.from_dict(chat_user_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


