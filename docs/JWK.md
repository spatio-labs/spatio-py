# JWK

A single JSON Web Key (RFC 7517 §4) — RSA public key.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kty** | **str** |  | 
**use** | **str** |  | 
**alg** | **str** |  | 
**kid** | **str** |  | 
**n** | **str** | Base64url-encoded RSA modulus. | 
**e** | **str** | Base64url-encoded RSA exponent. Almost always \&quot;AQAB\&quot;. | 

## Example

```python
from spatio.models.jwk import JWK

# TODO update the JSON string below
json = "{}"
# create an instance of JWK from a JSON string
jwk_instance = JWK.from_json(json)
# print the JSON string representation of the object
print(JWK.to_json())

# convert the object into a dict
jwk_dict = jwk_instance.to_dict()
# create an instance of JWK from a dict
jwk_from_dict = JWK.from_dict(jwk_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


