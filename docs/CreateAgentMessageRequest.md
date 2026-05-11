# CreateAgentMessageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 
**content** | **str** |  | 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_agent_message_request import CreateAgentMessageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAgentMessageRequest from a JSON string
create_agent_message_request_instance = CreateAgentMessageRequest.from_json(json)
# print the JSON string representation of the object
print(CreateAgentMessageRequest.to_json())

# convert the object into a dict
create_agent_message_request_dict = create_agent_message_request_instance.to_dict()
# create an instance of CreateAgentMessageRequest from a dict
create_agent_message_request_from_dict = CreateAgentMessageRequest.from_dict(create_agent_message_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


