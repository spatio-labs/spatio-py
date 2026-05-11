# CreateAgentConversationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_agent_conversation_request import CreateAgentConversationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAgentConversationRequest from a JSON string
create_agent_conversation_request_instance = CreateAgentConversationRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAgentConversationRequest.to_json())

# convert the object into a dict
create_agent_conversation_request_dict = create_agent_conversation_request_instance.to_dict()
# create an instance of CreateAgentConversationRequest from a dict
create_agent_conversation_request_from_dict = CreateAgentConversationRequest.from_dict(create_agent_conversation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


