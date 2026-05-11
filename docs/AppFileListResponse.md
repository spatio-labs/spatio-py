# AppFileListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**files** | **List[Dict[str, object]]** |  | 

## Example

```python
from spatio.models.app_file_list_response import AppFileListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AppFileListResponse from a JSON string
app_file_list_response_instance = AppFileListResponse.from_json(json)
# print the JSON string representation of the object
print(AppFileListResponse.to_json())

# convert the object into a dict
app_file_list_response_dict = app_file_list_response_instance.to_dict()
# create an instance of AppFileListResponse from a dict
app_file_list_response_from_dict = AppFileListResponse.from_dict(app_file_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


