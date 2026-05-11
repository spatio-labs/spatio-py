# AgentSessionContext

Identity bundle returned to the agent at SessionStart. One round-trip provides user + current org/workspace + connected accounts so the agent doesn't fish on its first turn. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**user** | **Dict[str, object]** |  | [optional] 
**current_organization** | **Dict[str, object]** |  | [optional] 
**current_workspace** | **Dict[str, object]** |  | [optional] 
**connected_accounts** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.agent_session_context import AgentSessionContext

# TODO update the JSON string below
json = "{}"
# create an instance of AgentSessionContext from a JSON string
agent_session_context_instance = AgentSessionContext.from_json(json)
# print the JSON string representation of the object
print(AgentSessionContext.to_json())

# convert the object into a dict
agent_session_context_dict = agent_session_context_instance.to_dict()
# create an instance of AgentSessionContext from a dict
agent_session_context_from_dict = AgentSessionContext.from_dict(agent_session_context_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


