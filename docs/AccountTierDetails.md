# AccountTierDetails

Per-tier capability + quota envelope. Numeric quotas use 0/-1 idioms; treat large negatives as \"unlimited.\"

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | **str** |  | 
**daily_api_calls** | **int** |  | [optional] 
**max_connected_accounts** | **int** |  | [optional] 
**max_email_sends_per_day** | **int** |  | [optional] 
**max_notes** | **int** |  | [optional] 
**max_sheets** | **int** |  | [optional] 
**max_slides** | **int** |  | [optional] 
**max_files** | **int** |  | [optional] 
**max_tasks** | **int** |  | [optional] 
**max_team_members** | **int** |  | [optional] 
**max_workspaces** | **int** |  | [optional] 
**storage_gb** | **int** |  | [optional] 
**has_automations** | **bool** |  | [optional] 
**has_advanced_automations** | **bool** |  | [optional] 
**has_full_api_access** | **bool** |  | [optional] 

## Example

```python
from spatio.models.account_tier_details import AccountTierDetails

# TODO update the JSON string below
json = "{}"
# create an instance of AccountTierDetails from a JSON string
account_tier_details_instance = AccountTierDetails.from_json(json)
# print the JSON string representation of the object
print(AccountTierDetails.to_json())

# convert the object into a dict
account_tier_details_dict = account_tier_details_instance.to_dict()
# create an instance of AccountTierDetails from a dict
account_tier_details_from_dict = AccountTierDetails.from_dict(account_tier_details_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


