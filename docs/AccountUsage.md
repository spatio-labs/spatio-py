# AccountUsage

Today's usage counters. Snapshot reflects the in-memory rollup; counts reset at UTC midnight.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_date** | **str** | Always &#x60;today&#x60; for the current-day rollup. | 
**api_calls** | **int** |  | [optional] 
**email_sends** | **int** |  | [optional] 
**notes_count** | **int** |  | [optional] 
**sheets_count** | **int** |  | [optional] 
**slides_count** | **int** |  | [optional] 
**files_count** | **int** |  | [optional] 
**tasks_count** | **int** |  | [optional] 

## Example

```python
from spatio.models.account_usage import AccountUsage

# TODO update the JSON string below
json = "{}"
# create an instance of AccountUsage from a JSON string
account_usage_instance = AccountUsage.from_json(json)
# print the JSON string representation of the object
print(AccountUsage.to_json())

# convert the object into a dict
account_usage_dict = account_usage_instance.to_dict()
# create an instance of AccountUsage from a dict
account_usage_from_dict = AccountUsage.from_dict(account_usage_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


