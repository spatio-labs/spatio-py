# MoveFileRequest

Move a single file to a target folder. Pass `folderId: null` to move to the account root. Bulk moves use `POST /v1/files/move`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**folder_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.move_file_request import MoveFileRequest

# TODO update the JSON string below
json = "{}"
# create an instance of MoveFileRequest from a JSON string
move_file_request_instance = MoveFileRequest.from_json(json)
# print the JSON string representation of the object
print(MoveFileRequest.to_json())

# convert the object into a dict
move_file_request_dict = move_file_request_instance.to_dict()
# create an instance of MoveFileRequest from a dict
move_file_request_from_dict = MoveFileRequest.from_dict(move_file_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


