# UpdateEmailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | [**Email**](Email.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.update_email_response import UpdateEmailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateEmailResponse from a JSON string
update_email_response_instance = UpdateEmailResponse.from_json(json)
# print the JSON string representation of the object
print(UpdateEmailResponse.to_json())

# convert the object into a dict
update_email_response_dict = update_email_response_instance.to_dict()
# create an instance of UpdateEmailResponse from a dict
update_email_response_from_dict = UpdateEmailResponse.from_dict(update_email_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


