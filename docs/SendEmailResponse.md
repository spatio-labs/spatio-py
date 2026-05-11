# SendEmailResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**message_id** | **str** |  | 
**thread_id** | **str** |  | [optional] 
**provider** | **str** |  | 
**error** | **str** |  | [optional] 

## Example

```python
from spatio.models.send_email_response import SendEmailResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SendEmailResponse from a JSON string
send_email_response_instance = SendEmailResponse.from_json(json)
# print the JSON string representation of the object
print(SendEmailResponse.to_json())

# convert the object into a dict
send_email_response_dict = send_email_response_instance.to_dict()
# create an instance of SendEmailResponse from a dict
send_email_response_from_dict = SendEmailResponse.from_dict(send_email_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


