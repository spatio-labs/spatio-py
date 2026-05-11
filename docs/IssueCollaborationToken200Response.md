# IssueCollaborationToken200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** | HS256 JWT, signed with the shared platform/worker secret. | 
**ws_url** | **str** | Base WebSocket URL of the Yjs worker. | 
**room** | **str** |  | [optional] 
**expires_at** | **datetime** |  | 
**expires_in** | **int** | Seconds until the token expires. | 

## Example

```python
from spatio.models.issue_collaboration_token200_response import IssueCollaborationToken200Response

# TODO update the JSON string below
json = "{}"
# create an instance of IssueCollaborationToken200Response from a JSON string
issue_collaboration_token200_response_instance = IssueCollaborationToken200Response.from_json(json)
# print the JSON string representation of the object
print(IssueCollaborationToken200Response.to_json())

# convert the object into a dict
issue_collaboration_token200_response_dict = issue_collaboration_token200_response_instance.to_dict()
# create an instance of IssueCollaborationToken200Response from a dict
issue_collaboration_token200_response_from_dict = IssueCollaborationToken200Response.from_dict(issue_collaboration_token200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


