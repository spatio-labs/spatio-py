# MoveEmailsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message_ids** | **List[str]** |  | 

## Example

```python
from spatio.models.move_emails_request import MoveEmailsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of MoveEmailsRequest from a JSON string
move_emails_request_instance = MoveEmailsRequest.from_json(json)
# print the JSON string representation of the object
print(MoveEmailsRequest.to_json())

# convert the object into a dict
move_emails_request_dict = move_emails_request_instance.to_dict()
# create an instance of MoveEmailsRequest from a dict
move_emails_request_from_dict = MoveEmailsRequest.from_dict(move_emails_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


