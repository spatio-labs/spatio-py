# SaveMessageRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**role** | **str** |  | 
**content** | **str** |  | 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.save_message_request import SaveMessageRequest

# TODO update the JSON string below
json = "{}"
# create an instance of SaveMessageRequest from a JSON string
save_message_request_instance = SaveMessageRequest.from_json(json)
# print the JSON string representation of the object
print(SaveMessageRequest.to_json())

# convert the object into a dict
save_message_request_dict = save_message_request_instance.to_dict()
# create an instance of SaveMessageRequest from a dict
save_message_request_from_dict = SaveMessageRequest.from_dict(save_message_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


