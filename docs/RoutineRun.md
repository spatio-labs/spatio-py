# RoutineRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**routine_id** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**progress** | **int** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**completed_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.routine_run import RoutineRun

# TODO update the JSON string below
json = "{}"
# create an instance of RoutineRun from a JSON string
routine_run_instance = RoutineRun.from_json(json)
# print the JSON string representation of the object
print(RoutineRun.to_json())

# convert the object into a dict
routine_run_dict = routine_run_instance.to_dict()
# create an instance of RoutineRun from a dict
routine_run_from_dict = RoutineRun.from_dict(routine_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


