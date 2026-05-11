# RoutineRunProgressRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**progress** | **int** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.routine_run_progress_request import RoutineRunProgressRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RoutineRunProgressRequest from a JSON string
routine_run_progress_request_instance = RoutineRunProgressRequest.from_json(json)
# print the JSON string representation of the object
print(RoutineRunProgressRequest.to_json())

# convert the object into a dict
routine_run_progress_request_dict = routine_run_progress_request_instance.to_dict()
# create an instance of RoutineRunProgressRequest from a dict
routine_run_progress_request_from_dict = RoutineRunProgressRequest.from_dict(routine_run_progress_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


