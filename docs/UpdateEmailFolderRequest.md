# UpdateEmailFolderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_email_folder_request import UpdateEmailFolderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEmailFolderRequest from a JSON string
update_email_folder_request_instance = UpdateEmailFolderRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateEmailFolderRequest.to_json())

# convert the object into a dict
update_email_folder_request_dict = update_email_folder_request_instance.to_dict()
# create an instance of UpdateEmailFolderRequest from a dict
update_email_folder_request_from_dict = UpdateEmailFolderRequest.from_dict(update_email_folder_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


