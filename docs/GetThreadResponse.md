# GetThreadResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**thread** | [**SpatioThread**](SpatioThread.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.get_thread_response import GetThreadResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetThreadResponse from a JSON string
get_thread_response_instance = GetThreadResponse.from_json(json)
# print the JSON string representation of the object
print(GetThreadResponse.to_json())

# convert the object into a dict
get_thread_response_dict = get_thread_response_instance.to_dict()
# create an instance of GetThreadResponse from a dict
get_thread_response_from_dict = GetThreadResponse.from_dict(get_thread_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


