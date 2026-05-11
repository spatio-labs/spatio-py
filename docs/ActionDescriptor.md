# ActionDescriptor

Action manifest entry surfaced by the agent platform. The `inputType`/`outputType` references point at internal Go types; treat them as opaque labels. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**canonical_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**input_type** | **str** |  | [optional] 
**output_type** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.action_descriptor import ActionDescriptor

# TODO update the JSON string below
json = "{}"
# create an instance of ActionDescriptor from a JSON string
action_descriptor_instance = ActionDescriptor.from_json(json)
# print the JSON string representation of the object
print(ActionDescriptor.to_json())

# convert the object into a dict
action_descriptor_dict = action_descriptor_instance.to_dict()
# create an instance of ActionDescriptor from a dict
action_descriptor_from_dict = ActionDescriptor.from_dict(action_descriptor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


