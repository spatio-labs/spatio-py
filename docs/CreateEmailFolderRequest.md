# CreateEmailFolderRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_email_folder_request import CreateEmailFolderRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateEmailFolderRequest from a JSON string
create_email_folder_request_instance = CreateEmailFolderRequest.from_json(json)
# print the JSON string representation of the object
print(CreateEmailFolderRequest.to_json())

# convert the object into a dict
create_email_folder_request_dict = create_email_folder_request_instance.to_dict()
# create an instance of CreateEmailFolderRequest from a dict
create_email_folder_request_from_dict = CreateEmailFolderRequest.from_dict(create_email_folder_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


