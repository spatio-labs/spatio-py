# UploadFileBase64Request


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**content** | **bytes** | Base64-encoded file bytes. | 
**mime_type** | **str** |  | 
**folder_id** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.upload_file_base64_request import UploadFileBase64Request

# TODO update the JSON string below
json = "{}"
# create an instance of UploadFileBase64Request from a JSON string
upload_file_base64_request_instance = UploadFileBase64Request.from_json(json)
# print the JSON string representation of the object
print(UploadFileBase64Request.to_json())

# convert the object into a dict
upload_file_base64_request_dict = upload_file_base64_request_instance.to_dict()
# create an instance of UploadFileBase64Request from a dict
upload_file_base64_request_from_dict = UploadFileBase64Request.from_dict(upload_file_base64_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


