# AccountError

Per-account failure attached to `AccountStatus.error` inside a fan-out `Envelope`. `code` is machine-readable and stable across releases for the canonical values (`auth_expired`, `rate_limited`, `provider_5xx`, `timeout`); `unknown` is a fallback and should not be relied on. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**code** | **str** |  | 
**message** | **str** |  | 

## Example

```python
from spatio.models.account_error import AccountError

# TODO update the JSON string below
json = "{}"
# create an instance of AccountError from a JSON string
account_error_instance = AccountError.from_json(json)
# print the JSON string representation of the object
print(AccountError.to_json())

# convert the object into a dict
account_error_dict = account_error_instance.to_dict()
# create an instance of AccountError from a dict
account_error_from_dict = AccountError.from_dict(account_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


