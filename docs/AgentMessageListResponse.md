# AgentMessageListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**messages** | [**List[AgentMessage]**](AgentMessage.md) |  | 
**total** | **int** |  | [optional] 

## Example

```python
from spatio.models.agent_message_list_response import AgentMessageListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AgentMessageListResponse from a JSON string
agent_message_list_response_instance = AgentMessageListResponse.from_json(json)
# print the JSON string representation of the object
print(AgentMessageListResponse.to_json())

# convert the object into a dict
agent_message_list_response_dict = agent_message_list_response_instance.to_dict()
# create an instance of AgentMessageListResponse from a dict
agent_message_list_response_from_dict = AgentMessageListResponse.from_dict(agent_message_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


