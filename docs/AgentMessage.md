# AgentMessage


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**conversation_id** | **str** |  | [optional] 
**role** | **str** |  | 
**content** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.agent_message import AgentMessage

# TODO update the JSON string below
json = "{}"
# create an instance of AgentMessage from a JSON string
agent_message_instance = AgentMessage.from_json(json)
# print the JSON string representation of the object
print(AgentMessage.to_json())

# convert the object into a dict
agent_message_dict = agent_message_instance.to_dict()
# create an instance of AgentMessage from a dict
agent_message_from_dict = AgentMessage.from_dict(agent_message_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


