# EmailFolderListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**folders** | [**List[EmailFolder]**](EmailFolder.md) |  | 

## Example

```python
from spatio.models.email_folder_list_response import EmailFolderListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EmailFolderListResponse from a JSON string
email_folder_list_response_instance = EmailFolderListResponse.from_json(json)
# print the JSON string representation of the object
print(EmailFolderListResponse.to_json())

# convert the object into a dict
email_folder_list_response_dict = email_folder_list_response_instance.to_dict()
# create an instance of EmailFolderListResponse from a dict
email_folder_list_response_from_dict = EmailFolderListResponse.from_dict(email_folder_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


