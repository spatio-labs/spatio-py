# AgentConversationListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conversations** | [**List[AgentConversation]**](AgentConversation.md) |  | 
**total** | **int** |  | [optional] 

## Example

```python
from spatio.models.agent_conversation_list_response import AgentConversationListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AgentConversationListResponse from a JSON string
agent_conversation_list_response_instance = AgentConversationListResponse.from_json(json)
# print the JSON string representation of the object
print(AgentConversationListResponse.to_json())

# convert the object into a dict
agent_conversation_list_response_dict = agent_conversation_list_response_instance.to_dict()
# create an instance of AgentConversationListResponse from a dict
agent_conversation_list_response_from_dict = AgentConversationListResponse.from_dict(agent_conversation_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


