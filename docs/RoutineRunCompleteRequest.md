# RoutineRunCompleteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.routine_run_complete_request import RoutineRunCompleteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RoutineRunCompleteRequest from a JSON string
routine_run_complete_request_instance = RoutineRunCompleteRequest.from_json(json)
# print the JSON string representation of the object
print(RoutineRunCompleteRequest.to_json())

# convert the object into a dict
routine_run_complete_request_dict = routine_run_complete_request_instance.to_dict()
# create an instance of RoutineRunCompleteRequest from a dict
routine_run_complete_request_from_dict = RoutineRunCompleteRequest.from_dict(routine_run_complete_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


