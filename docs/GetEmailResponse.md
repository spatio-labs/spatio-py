# GetEmailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**email** | [**Email**](Email.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.get_email_response import GetEmailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of GetEmailResponse from a JSON string
get_email_response_instance = GetEmailResponse.from_json(json)
# print the JSON string representation of the object
print(GetEmailResponse.to_json())

# convert the object into a dict
get_email_response_dict = get_email_response_instance.to_dict()
# create an instance of GetEmailResponse from a dict
get_email_response_from_dict = GetEmailResponse.from_dict(get_email_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


