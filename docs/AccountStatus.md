# AccountStatus

Outcome of one connected account's contribution to a fan-out call. Every connection that participated appears in `Envelope.accounts` exactly once, regardless of whether it succeeded, errored, or returned zero items. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** | Provider id (e.g. &#x60;native-notes&#x60;, &#x60;notion&#x60;, &#x60;google-keep&#x60;). | 
**account_id** | **str** | Connected-account row id. | 
**account_name** | **str** | Human-readable label for the account, when available. | [optional] 
**status** | **str** | - &#x60;ok&#x60; — provider call returned without error. - &#x60;error&#x60; — provider call failed; details in &#x60;error&#x60;. - &#x60;skipped&#x60; — connection was filtered out before the provider   call ran. Reserved; not currently emitted by the runtime.  | 
**error** | [**AccountError**](AccountError.md) |  | [optional] 
**next_page_token** | **str** | Provider-specific cursor for the next page, if any. | [optional] 

## Example

```python
from spatio.models.account_status import AccountStatus

# TODO update the JSON string below
json = "{}"
# create an instance of AccountStatus from a JSON string
account_status_instance = AccountStatus.from_json(json)
# print the JSON string representation of the object
print(AccountStatus.to_json())

# convert the object into a dict
account_status_dict = account_status_instance.to_dict()
# create an instance of AccountStatus from a dict
account_status_from_dict = AccountStatus.from_dict(account_status_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


