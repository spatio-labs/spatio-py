# ReplyEmailRequest

Reply to a specific email. `to/cc/bcc` are optional — the platform falls back to the original sender / recipients when omitted. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**to** | **List[str]** |  | [optional] 
**cc** | **List[str]** |  | [optional] 
**bcc** | **List[str]** |  | [optional] 
**body** | **str** |  | 
**html** | **bool** |  | [optional] 
**attachments** | [**List[AttachmentInput]**](AttachmentInput.md) |  | [optional] 

## Example

```python
from spatio.models.reply_email_request import ReplyEmailRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ReplyEmailRequest from a JSON string
reply_email_request_instance = ReplyEmailRequest.from_json(json)
# print the JSON string representation of the object
print(ReplyEmailRequest.to_json())

# convert the object into a dict
reply_email_request_dict = reply_email_request_instance.to_dict()
# create an instance of ReplyEmailRequest from a dict
reply_email_request_from_dict = ReplyEmailRequest.from_dict(reply_email_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


