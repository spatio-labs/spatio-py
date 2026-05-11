# IssueCollaborationTokenRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**room** | **str** | Optional &#x60;&lt;type&gt;:&lt;id&gt;&#x60; room identifier (e.g. &#x60;note:abc123&#x60;). When set, the JWT only authorizes this single room.  | [optional] 

## Example

```python
from spatio.models.issue_collaboration_token_request import IssueCollaborationTokenRequest

# TODO update the JSON string below
json = "{}"
# create an instance of IssueCollaborationTokenRequest from a JSON string
issue_collaboration_token_request_instance = IssueCollaborationTokenRequest.from_json(json)
# print the JSON string representation of the object
print(IssueCollaborationTokenRequest.to_json())

# convert the object into a dict
issue_collaboration_token_request_dict = issue_collaboration_token_request_instance.to_dict()
# create an instance of IssueCollaborationTokenRequest from a dict
issue_collaboration_token_request_from_dict = IssueCollaborationTokenRequest.from_dict(issue_collaboration_token_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


