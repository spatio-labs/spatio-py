# CreateDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**to** | **List[str]** |  | [optional] 
**cc** | **List[str]** |  | [optional] 
**bcc** | **List[str]** |  | [optional] 
**subject** | **str** |  | [optional] 
**body** | **str** |  | [optional] 
**html** | **bool** |  | [optional] 
**attachments** | [**List[AttachmentInput]**](AttachmentInput.md) |  | [optional] 
**thread_id** | **str** | Provider thread id — set when this draft is a reply, so the sent message lands inside the parent thread.  | [optional] 
**in_reply_to** | **str** |  | [optional] 
**references** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.create_draft_request import CreateDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateDraftRequest from a JSON string
create_draft_request_instance = CreateDraftRequest.from_json(json)
# print the JSON string representation of the object
print(CreateDraftRequest.to_json())

# convert the object into a dict
create_draft_request_dict = create_draft_request_instance.to_dict()
# create an instance of CreateDraftRequest from a dict
create_draft_request_from_dict = CreateDraftRequest.from_dict(create_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


