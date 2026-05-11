# QuotaExceededError

Returned by upload endpoints when the caller's storage quota is exhausted. `code: quota_exceeded` is reserved. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Human-readable error message. | 
**code** | **str** | Machine-readable error code. Stable across releases for the canonical codes (&#x60;ambiguous_account&#x60;, &#x60;no_notes_provider&#x60;, &#x60;note_not_found&#x60;). Absent for generic errors.  | [optional] 

## Example

```python
from spatio.models.quota_exceeded_error import QuotaExceededError

# TODO update the JSON string below
json = "{}"
# create an instance of QuotaExceededError from a JSON string
quota_exceeded_error_instance = QuotaExceededError.from_json(json)
# print the JSON string representation of the object
print(QuotaExceededError.to_json())

# convert the object into a dict
quota_exceeded_error_dict = quota_exceeded_error_instance.to_dict()
# create an instance of QuotaExceededError from a dict
quota_exceeded_error_from_dict = QuotaExceededError.from_dict(quota_exceeded_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


