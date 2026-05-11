# RoutineListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Routine]**](Routine.md) |  | 

## Example

```python
from spatio.models.routine_list_response import RoutineListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RoutineListResponse from a JSON string
routine_list_response_instance = RoutineListResponse.from_json(json)
# print the JSON string representation of the object
print(RoutineListResponse.to_json())

# convert the object into a dict
routine_list_response_dict = routine_list_response_instance.to_dict()
# create an instance of RoutineListResponse from a dict
routine_list_response_from_dict = RoutineListResponse.from_dict(routine_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


