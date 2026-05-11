# SpatioThread


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**messages** | [**List[Email]**](Email.md) |  | 
**snippet** | **str** |  | [optional] 
**labels** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.spatio_thread import SpatioThread

# TODO update the JSON string below
json = "{}"
# create an instance of SpatioThread from a JSON string
spatio_thread_instance = SpatioThread.from_json(json)
# print the JSON string representation of the object
print(SpatioThread.to_json())

# convert the object into a dict
spatio_thread_dict = spatio_thread_instance.to_dict()
# create an instance of SpatioThread from a dict
spatio_thread_from_dict = SpatioThread.from_dict(spatio_thread_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


