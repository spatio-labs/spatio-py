# PersonalAccessToken


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**scopes** | **List[str]** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**last_used_at** | **datetime** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 
**token_prefix** | **str** |  | [optional] 

## Example

```python
from spatio.models.personal_access_token import PersonalAccessToken

# TODO update the JSON string below
json = "{}"
# create an instance of PersonalAccessToken from a JSON string
personal_access_token_instance = PersonalAccessToken.from_json(json)
# print the JSON string representation of the object
print(PersonalAccessToken.to_json())

# convert the object into a dict
personal_access_token_dict = personal_access_token_instance.to_dict()
# create an instance of PersonalAccessToken from a dict
personal_access_token_from_dict = PersonalAccessToken.from_dict(personal_access_token_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


