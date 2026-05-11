# PasswordRequiredError

Returned by `GET /public/notes/{token}` when the note is password-protected. `requiresPassword` is always `true` in this response; `invalidPassword` is `true` only when a password was supplied and rejected. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Human-readable error message. | 
**code** | **str** | Machine-readable error code. Stable across releases for the canonical codes (&#x60;ambiguous_account&#x60;, &#x60;no_notes_provider&#x60;, &#x60;note_not_found&#x60;). Absent for generic errors.  | [optional] 
**requires_password** | **bool** |  | 
**invalid_password** | **bool** |  | [optional] 

## Example

```python
from spatio.models.password_required_error import PasswordRequiredError

# TODO update the JSON string below
json = "{}"
# create an instance of PasswordRequiredError from a JSON string
password_required_error_instance = PasswordRequiredError.from_json(json)
# print the JSON string representation of the object
print(PasswordRequiredError.to_json())

# convert the object into a dict
password_required_error_dict = password_required_error_instance.to_dict()
# create an instance of PasswordRequiredError from a dict
password_required_error_from_dict = PasswordRequiredError.from_dict(password_required_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


