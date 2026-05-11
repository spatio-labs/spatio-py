# DiscoveryDocument

OAuth 2.1 (RFC 8414) + OpenID Connect Discovery 1.0 metadata. Same payload returned from both well-known paths. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**issuer** | **str** |  | 
**authorization_endpoint** | **str** |  | 
**token_endpoint** | **str** |  | 
**registration_endpoint** | **str** |  | [optional] 
**introspection_endpoint** | **str** |  | [optional] 
**revocation_endpoint** | **str** |  | [optional] 
**userinfo_endpoint** | **str** |  | [optional] 
**jwks_uri** | **str** |  | 
**response_types_supported** | **List[str]** |  | [optional] 
**grant_types_supported** | **List[str]** |  | [optional] 
**token_endpoint_auth_methods_supported** | **List[str]** |  | [optional] 
**code_challenge_methods_supported** | **List[str]** |  | [optional] 
**scopes_supported** | **List[str]** |  | 
**subject_types_supported** | **List[str]** |  | [optional] 
**id_token_signing_alg_values_supported** | **List[str]** |  | [optional] 
**prompt_values_supported** | **List[str]** |  | [optional] 
**claims_supported** | **List[str]** |  | [optional] 
**service_documentation** | **str** |  | [optional] 

## Example

```python
from spatio.models.discovery_document import DiscoveryDocument

# TODO update the JSON string below
json = "{}"
# create an instance of DiscoveryDocument from a JSON string
discovery_document_instance = DiscoveryDocument.from_json(json)
# print the JSON string representation of the object
print(DiscoveryDocument.to_json())

# convert the object into a dict
discovery_document_dict = discovery_document_instance.to_dict()
# create an instance of DiscoveryDocument from a dict
discovery_document_from_dict = DiscoveryDocument.from_dict(discovery_document_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


