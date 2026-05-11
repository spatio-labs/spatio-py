# AccountPlan

Subscription summary. `tier` is the canonical billing tier (uppercased: `FREE`, `PRO`, `MAX`, `ENTERPRISE`); `display_name` is the lowercase user-facing label. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | **str** |  | 
**display_name** | **str** |  | 
**subscription_status** | **str** | Stripe subscription state: &#x60;ACTIVE&#x60;, &#x60;TRIALING&#x60;, &#x60;PAST_DUE&#x60;, &#x60;CANCELED&#x60;, etc. | 
**trial_ends_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.account_plan import AccountPlan

# TODO update the JSON string below
json = "{}"
# create an instance of AccountPlan from a JSON string
account_plan_instance = AccountPlan.from_json(json)
# print the JSON string representation of the object
print(AccountPlan.to_json())

# convert the object into a dict
account_plan_dict = account_plan_instance.to_dict()
# create an instance of AccountPlan from a dict
account_plan_from_dict = AccountPlan.from_dict(account_plan_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


