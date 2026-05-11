# Conversation

LLM conversation persisted by the platform-service. Stored in snake_case at the wire (legacy DTO; predates the camelCase rest of the API). Treat field names as authoritative. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**user_id** | **str** |  | 
**title** | **str** |  | 
**context** | **str** | Free-form context tag (e.g. &#x60;sidebar:sheets:entity:&lt;id&gt;&#x60;). | [optional] 
**cwd** | **str** |  | [optional] 
**session_id** | **str** |  | [optional] 
**pinned** | **bool** |  | [optional] 
**last_message_at** | **datetime** |  | [optional] 
**message_count** | **int** |  | [optional] 
**is_active** | **bool** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.conversation import Conversation

# TODO update the JSON string below
json = "{}"
# create an instance of Conversation from a JSON string
conversation_instance = Conversation.from_json(json)
# print the JSON string representation of the object
print(Conversation.to_json())

# convert the object into a dict
conversation_dict = conversation_instance.to_dict()
# create an instance of Conversation from a dict
conversation_from_dict = Conversation.from_dict(conversation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


