# AppFileContentResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **str** |  | 
**content** | **str** |  | [optional] 

## Example

```python
from spatio.models.app_file_content_response import AppFileContentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AppFileContentResponse from a JSON string
app_file_content_response_instance = AppFileContentResponse.from_json(json)
# print the JSON string representation of the object
print(AppFileContentResponse.to_json())

# convert the object into a dict
app_file_content_response_dict = app_file_content_response_instance.to_dict()
# create an instance of AppFileContentResponse from a dict
app_file_content_response_from_dict = AppFileContentResponse.from_dict(app_file_content_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


