# Routine


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**workspace_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**schedule** | **Dict[str, object]** |  | [optional] 
**status** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.routine import Routine

# TODO update the JSON string below
json = "{}"
# create an instance of Routine from a JSON string
routine_instance = Routine.from_json(json)
# print the JSON string representation of the object
print(Routine.to_json())

# convert the object into a dict
routine_dict = routine_instance.to_dict()
# create an instance of Routine from a dict
routine_from_dict = Routine.from_dict(routine_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


