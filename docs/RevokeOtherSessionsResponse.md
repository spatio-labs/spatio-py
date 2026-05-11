# RevokeOtherSessionsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revoked** | **int** | Count of sessions revoked. | [optional] 

## Example

```python
from spatio.models.revoke_other_sessions_response import RevokeOtherSessionsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RevokeOtherSessionsResponse from a JSON string
revoke_other_sessions_response_instance = RevokeOtherSessionsResponse.from_json(json)
# print the JSON string representation of the object
print(RevokeOtherSessionsResponse.to_json())

# convert the object into a dict
revoke_other_sessions_response_dict = revoke_other_sessions_response_instance.to_dict()
# create an instance of RevokeOtherSessionsResponse from a dict
revoke_other_sessions_response_from_dict = RevokeOtherSessionsResponse.from_dict(revoke_other_sessions_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


