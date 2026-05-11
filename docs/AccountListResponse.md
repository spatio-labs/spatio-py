# AccountListResponse

`GET /v1/accounts` returns `{accounts_by_platform, total_accounts}` on production today. Schema kept open until the consumers migrate to a flat `accounts` array. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**accounts_by_platform** | **Dict[str, object]** |  | [optional] 
**total_accounts** | **int** |  | [optional] 
**accounts** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.account_list_response import AccountListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of AccountListResponse from a JSON string
account_list_response_instance = AccountListResponse.from_json(json)
# print the JSON string representation of the object
print(AccountListResponse.to_json())

# convert the object into a dict
account_list_response_dict = account_list_response_instance.to_dict()
# create an instance of AccountListResponse from a dict
account_list_response_from_dict = AccountListResponse.from_dict(account_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


