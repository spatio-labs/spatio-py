# AmbiguousAccountError

Returned when the caller's request matches more than one connected account and no `accountId` query param disambiguates which one to target. The `accounts` array enumerates the candidates so the client can prompt the user to pick. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Human-readable error message. | 
**code** | **str** | Machine-readable error code. Stable across releases for the canonical codes (&#x60;ambiguous_account&#x60;, &#x60;no_notes_provider&#x60;, &#x60;note_not_found&#x60;). Absent for generic errors.  | [optional] 
**accounts** | [**List[AccountChoice]**](AccountChoice.md) |  | [optional] 

## Example

```python
from spatio.models.ambiguous_account_error import AmbiguousAccountError

# TODO update the JSON string below
json = "{}"
# create an instance of AmbiguousAccountError from a JSON string
ambiguous_account_error_instance = AmbiguousAccountError.from_json(json)
# print the JSON string representation of the object
print(AmbiguousAccountError.to_json())

# convert the object into a dict
ambiguous_account_error_dict = ambiguous_account_error_instance.to_dict()
# create an instance of AmbiguousAccountError from a dict
ambiguous_account_error_from_dict = AmbiguousAccountError.from_dict(ambiguous_account_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


