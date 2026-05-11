# ExecuteChatActionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**result** | **object** | Action-specific result payload. | [optional] 

## Example

```python
from spatio.models.execute_chat_action_response import ExecuteChatActionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ExecuteChatActionResponse from a JSON string
execute_chat_action_response_instance = ExecuteChatActionResponse.from_json(json)
# print the JSON string representation of the object
print(ExecuteChatActionResponse.to_json())

# convert the object into a dict
execute_chat_action_response_dict = execute_chat_action_response_instance.to_dict()
# create an instance of ExecuteChatActionResponse from a dict
execute_chat_action_response_from_dict = ExecuteChatActionResponse.from_dict(execute_chat_action_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


