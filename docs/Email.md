# Email

A single email message. The `provider`/`accountId` provenance fields tell clients which connected mail account this row came from (Gmail, Outlook, etc.) so multi-account list responses can be merged sensibly client-side. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**thread_id** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**subject** | **str** |  | 
**var_from** | **str** |  | 
**to** | **List[str]** |  | 
**cc** | **List[str]** |  | [optional] 
**bcc** | **List[str]** |  | [optional] 
**body** | **str** |  | 
**html** | **bool** | &#x60;true&#x60; when &#x60;body&#x60; contains HTML, &#x60;false&#x60; for plain text.  | 
**var_date** | **datetime** |  | 
**labels** | **List[str]** |  | [optional] 
**is_read** | **bool** |  | 
**is_starred** | **bool** |  | 
**attachments** | [**List[AttachmentMeta]**](AttachmentMeta.md) |  | [optional] 
**snippet** | **str** |  | [optional] 
**message_id** | **str** | RFC 5322 Message-ID header. | [optional] 
**in_reply_to** | **str** | RFC 5322 In-Reply-To header — the parent message id this message is a reply to.  | [optional] 
**references** | **List[str]** | RFC 5322 References header (ancestor chain). | [optional] 

## Example

```python
from spatio.models.email import Email

# TODO update the JSON string below
json = "{}"
# create an instance of Email from a JSON string
email_instance = Email.from_json(json)
# print the JSON string representation of the object
print(Email.to_json())

# convert the object into a dict
email_dict = email_instance.to_dict()
# create an instance of Email from a dict
email_from_dict = Email.from_dict(email_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


