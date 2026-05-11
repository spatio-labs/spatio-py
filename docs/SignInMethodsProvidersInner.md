# SignInMethodsProvidersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** | OAuth IdP: &#x60;GOOGLE&#x60;, &#x60;GITHUB&#x60;, etc. | 
**account_email** | **str** |  | [optional] 
**linked_at** | **datetime** |  | [optional] 
**last_used_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.sign_in_methods_providers_inner import SignInMethodsProvidersInner

# TODO update the JSON string below
json = "{}"
# create an instance of SignInMethodsProvidersInner from a JSON string
sign_in_methods_providers_inner_instance = SignInMethodsProvidersInner.from_json(json)
# print the JSON string representation of the object
print(SignInMethodsProvidersInner.to_json())

# convert the object into a dict
sign_in_methods_providers_inner_dict = sign_in_methods_providers_inner_instance.to_dict()
# create an instance of SignInMethodsProvidersInner from a dict
sign_in_methods_providers_inner_from_dict = SignInMethodsProvidersInner.from_dict(sign_in_methods_providers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


