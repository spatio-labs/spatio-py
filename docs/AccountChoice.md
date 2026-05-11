# AccountChoice

One of the candidates returned alongside an `ambiguous_account` error so the client can prompt the user to pick a target account. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** |  | 
**account_id** | **str** |  | 
**account_name** | **str** |  | [optional] 

## Example

```python
from spatio.models.account_choice import AccountChoice

# TODO update the JSON string below
json = "{}"
# create an instance of AccountChoice from a JSON string
account_choice_instance = AccountChoice.from_json(json)
# print the JSON string representation of the object
print(AccountChoice.to_json())

# convert the object into a dict
account_choice_dict = account_choice_instance.to_dict()
# create an instance of AccountChoice from a dict
account_choice_from_dict = AccountChoice.from_dict(account_choice_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


