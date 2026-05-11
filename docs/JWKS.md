# JWKS


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keys** | [**List[JWK]**](JWK.md) |  | 

## Example

```python
from spatio.models.jwks import JWKS

# TODO update the JSON string below
json = "{}"
# create an instance of JWKS from a JSON string
jwks_instance = JWKS.from_json(json)
# print the JSON string representation of the object
print(JWKS.to_json())

# convert the object into a dict
jwks_dict = jwks_instance.to_dict()
# create an instance of JWKS from a dict
jwks_from_dict = JWKS.from_dict(jwks_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


