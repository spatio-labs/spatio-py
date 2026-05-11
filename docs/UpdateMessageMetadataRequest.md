# UpdateMessageMetadataRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.update_message_metadata_request import UpdateMessageMetadataRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateMessageMetadataRequest from a JSON string
update_message_metadata_request_instance = UpdateMessageMetadataRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateMessageMetadataRequest.to_json())

# convert the object into a dict
update_message_metadata_request_dict = update_message_metadata_request_instance.to_dict()
# create an instance of UpdateMessageMetadataRequest from a dict
update_message_metadata_request_from_dict = UpdateMessageMetadataRequest.from_dict(update_message_metadata_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


