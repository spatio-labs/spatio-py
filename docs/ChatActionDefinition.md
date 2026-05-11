# ChatActionDefinition

One entry in `GET /actions`. Action ids are dotted (e.g. `direct-messages.send`, `channels.list`); the `executeAction` endpoint accepts the id with a free-form `params` object. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**platform** | **str** |  | 
**category** | **str** | Common values: &#x60;read&#x60;, &#x60;write&#x60;, &#x60;delete&#x60;, &#x60;manage&#x60;, &#x60;sync&#x60;. | [optional] 
**input_type** | **str** |  | [optional] 
**output_type** | **str** |  | [optional] 
**scopes** | **List[str]** | &#x60;null&#x60; when no scopes are declared (Go nil-slice). | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.chat_action_definition import ChatActionDefinition

# TODO update the JSON string below
json = "{}"
# create an instance of ChatActionDefinition from a JSON string
chat_action_definition_instance = ChatActionDefinition.from_json(json)
# print the JSON string representation of the object
print(ChatActionDefinition.to_json())

# convert the object into a dict
chat_action_definition_dict = chat_action_definition_instance.to_dict()
# create an instance of ChatActionDefinition from a dict
chat_action_definition_from_dict = ChatActionDefinition.from_dict(chat_action_definition_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


