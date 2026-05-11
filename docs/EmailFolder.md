# EmailFolder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.email_folder import EmailFolder

# TODO update the JSON string below
json = "{}"
# create an instance of EmailFolder from a JSON string
email_folder_instance = EmailFolder.from_json(json)
# print the JSON string representation of the object
print(EmailFolder.to_json())

# convert the object into a dict
email_folder_dict = email_folder_instance.to_dict()
# create an instance of EmailFolder from a dict
email_folder_from_dict = EmailFolder.from_dict(email_folder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


