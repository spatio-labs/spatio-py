# PreconfiguredAgent

Curated featured agents — read-only, surfaced by the renderer's \"preconfigured\" picker. Not full Agent records; minimal display metadata only. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**agent_id** | **str** |  | 
**name** | **str** |  | 
**tagline** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**has_all_tools** | **bool** |  | [optional] 
**tool_count** | **int** |  | [optional] 

## Example

```python
from spatio.models.preconfigured_agent import PreconfiguredAgent

# TODO update the JSON string below
json = "{}"
# create an instance of PreconfiguredAgent from a JSON string
preconfigured_agent_instance = PreconfiguredAgent.from_json(json)
# print the JSON string representation of the object
print(PreconfiguredAgent.to_json())

# convert the object into a dict
preconfigured_agent_dict = preconfigured_agent_instance.to_dict()
# create an instance of PreconfiguredAgent from a dict
preconfigured_agent_from_dict = PreconfiguredAgent.from_dict(preconfigured_agent_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


