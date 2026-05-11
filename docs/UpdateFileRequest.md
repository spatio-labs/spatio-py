# UpdateFileRequest

Partial update.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**folder_id** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.update_file_request import UpdateFileRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateFileRequest from a JSON string
update_file_request_instance = UpdateFileRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateFileRequest.to_json())

# convert the object into a dict
update_file_request_dict = update_file_request_instance.to_dict()
# create an instance of UpdateFileRequest from a dict
update_file_request_from_dict = UpdateFileRequest.from_dict(update_file_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


