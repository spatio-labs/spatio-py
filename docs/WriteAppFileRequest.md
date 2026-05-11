# WriteAppFileRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **str** |  | 
**content** | **str** |  | 

## Example

```python
from spatio.models.write_app_file_request import WriteAppFileRequest

# TODO update the JSON string below
json = "{}"
# create an instance of WriteAppFileRequest from a JSON string
write_app_file_request_instance = WriteAppFileRequest.from_json(json)
# print the JSON string representation of the object
print(WriteAppFileRequest.to_json())

# convert the object into a dict
write_app_file_request_dict = write_app_file_request_instance.to_dict()
# create an instance of WriteAppFileRequest from a dict
write_app_file_request_from_dict = WriteAppFileRequest.from_dict(write_app_file_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


