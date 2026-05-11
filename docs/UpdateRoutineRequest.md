# UpdateRoutineRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**schedule** | **Dict[str, object]** |  | [optional] 
**status** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.update_routine_request import UpdateRoutineRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRoutineRequest from a JSON string
update_routine_request_instance = UpdateRoutineRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRoutineRequest.to_json())

# convert the object into a dict
update_routine_request_dict = update_routine_request_instance.to_dict()
# create an instance of UpdateRoutineRequest from a dict
update_routine_request_from_dict = UpdateRoutineRequest.from_dict(update_routine_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


