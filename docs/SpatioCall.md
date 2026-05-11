# SpatioCall


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**title** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**host_user_id** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**room_id** | **str** |  | [optional] 
**participants** | **List[Dict[str, object]]** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**started_at** | **datetime** |  | [optional] 
**ended_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.spatio_call import SpatioCall

# TODO update the JSON string below
json = "{}"
# create an instance of SpatioCall from a JSON string
spatio_call_instance = SpatioCall.from_json(json)
# print the JSON string representation of the object
print(SpatioCall.to_json())

# convert the object into a dict
spatio_call_dict = spatio_call_instance.to_dict()
# create an instance of SpatioCall from a dict
spatio_call_from_dict = SpatioCall.from_dict(spatio_call_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


