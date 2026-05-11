# CoreAction

Renderer-curated \"core action\" entry. These are the keyboard + command-palette surfaced actions; superset of the platform-tagged agent actions. Schema kept open since the platform metadata varies by category. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**platform** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.core_action import CoreAction

# TODO update the JSON string below
json = "{}"
# create an instance of CoreAction from a JSON string
core_action_instance = CoreAction.from_json(json)
# print the JSON string representation of the object
print(CoreAction.to_json())

# convert the object into a dict
core_action_dict = core_action_instance.to_dict()
# create an instance of CoreAction from a dict
core_action_from_dict = CoreAction.from_dict(core_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


