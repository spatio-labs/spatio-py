# ExecuteChatActionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**action_id** | **str** |  | 
**params** | **object** | Action-specific parameters. Free-form because the shape depends on &#x60;action_id&#x60;. See &#x60;GET /actions&#x60; for the per-id contract.  | [optional] 

## Example

```python
from spatio.models.execute_chat_action_request import ExecuteChatActionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ExecuteChatActionRequest from a JSON string
execute_chat_action_request_instance = ExecuteChatActionRequest.from_json(json)
# print the JSON string representation of the object
print(ExecuteChatActionRequest.to_json())

# convert the object into a dict
execute_chat_action_request_dict = execute_chat_action_request_instance.to_dict()
# create an instance of ExecuteChatActionRequest from a dict
execute_chat_action_request_from_dict = ExecuteChatActionRequest.from_dict(execute_chat_action_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


