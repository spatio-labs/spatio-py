# ChatActionsList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | [**List[ChatActionDefinition]**](ChatActionDefinition.md) |  | 

## Example

```python
from spatio.models.chat_actions_list import ChatActionsList

# TODO update the JSON string below
json = "{}"
# create an instance of ChatActionsList from a JSON string
chat_actions_list_instance = ChatActionsList.from_json(json)
# print the JSON string representation of the object
print(ChatActionsList.to_json())

# convert the object into a dict
chat_actions_list_dict = chat_actions_list_instance.to_dict()
# create an instance of ChatActionsList from a dict
chat_actions_list_from_dict = ChatActionsList.from_dict(chat_actions_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


