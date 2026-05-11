# RoutineRunListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[RoutineRun]**](RoutineRun.md) |  | 

## Example

```python
from spatio.models.routine_run_list_response import RoutineRunListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RoutineRunListResponse from a JSON string
routine_run_list_response_instance = RoutineRunListResponse.from_json(json)
# print the JSON string representation of the object
print(RoutineRunListResponse.to_json())

# convert the object into a dict
routine_run_list_response_dict = routine_run_list_response_instance.to_dict()
# create an instance of RoutineRunListResponse from a dict
routine_run_list_response_from_dict = RoutineRunListResponse.from_dict(routine_run_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


