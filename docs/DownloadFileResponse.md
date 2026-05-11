# DownloadFileResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**signed_url** | **str** | Pre-signed direct-download URL pointing at the backing storage (R2, Drive, etc.). Time-limited per provider. Clients follow the URL — the platform does not proxy bytes.  | 
**file** | [**SpatioFile**](SpatioFile.md) |  | 

## Example

```python
from spatio.models.download_file_response import DownloadFileResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DownloadFileResponse from a JSON string
download_file_response_instance = DownloadFileResponse.from_json(json)
# print the JSON string representation of the object
print(DownloadFileResponse.to_json())

# convert the object into a dict
download_file_response_dict = download_file_response_instance.to_dict()
# create an instance of DownloadFileResponse from a dict
download_file_response_from_dict = DownloadFileResponse.from_dict(download_file_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


