# CoreActionListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**actions** | [**List[CoreAction]**](CoreAction.md) |  | 
**total** | **int** |  | [optional] 

## Example

```python
from spatio.models.core_action_list_response import CoreActionListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CoreActionListResponse from a JSON string
core_action_list_response_instance = CoreActionListResponse.from_json(json)
# print the JSON string representation of the object
print(CoreActionListResponse.to_json())

# convert the object into a dict
core_action_list_response_dict = core_action_list_response_instance.to_dict()
# create an instance of CoreActionListResponse from a dict
core_action_list_response_from_dict = CoreActionListResponse.from_dict(core_action_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


