# UserInfoResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**sub** | **str** | User identifier (stable for the lifetime of the user). | 
**email** | **str** |  | [optional] 
**email_verified** | **bool** |  | [optional] 
**name** | **str** |  | [optional] 
**given_name** | **str** |  | [optional] 
**family_name** | **str** |  | [optional] 
**preferred_username** | **str** |  | [optional] 
**picture** | **str** |  | [optional] 
**updated_at** | **int** |  | [optional] 

## Example

```python
from spatio.models.user_info_response import UserInfoResponse

# TODO update the JSON string below
json = "{}"
# create an instance of UserInfoResponse from a JSON string
user_info_response_instance = UserInfoResponse.from_json(json)
# print the JSON string representation of the object
print(UserInfoResponse.to_json())

# convert the object into a dict
user_info_response_dict = user_info_response_instance.to_dict()
# create an instance of UserInfoResponse from a dict
user_info_response_from_dict = UserInfoResponse.from_dict(user_info_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


