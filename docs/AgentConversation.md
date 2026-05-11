# AgentConversation

LLM conversation tracked by the agent platform (distinct from /v1/conversations which is the renderer-driven sidebar persistence). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**agent_id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.agent_conversation import AgentConversation

# TODO update the JSON string below
json = "{}"
# create an instance of AgentConversation from a JSON string
agent_conversation_instance = AgentConversation.from_json(json)
# print the JSON string representation of the object
print(AgentConversation.to_json())

# convert the object into a dict
agent_conversation_dict = agent_conversation_instance.to_dict()
# create an instance of AgentConversation from a dict
agent_conversation_from_dict = AgentConversation.from_dict(agent_conversation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


