# TokenResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**access_token** | **str** | Opaque bearer token. Format &#x60;tok_&lt;32 random base64url&gt;&#x60;. | 
**token_type** | **str** |  | 
**expires_in** | **int** | Seconds until access_token expires. | 
**refresh_token** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 
**id_token** | **str** | Only present when &#x60;openid&#x60; scope was granted. RS256-signed JWT — verify against the JWKS. | [optional] 

## Example

```python
from spatio.models.token_response import TokenResponse

# TODO update the JSON string below
json = "{}"
# create an instance of TokenResponse from a JSON string
token_response_instance = TokenResponse.from_json(json)
# print the JSON string representation of the object
print(TokenResponse.to_json())

# convert the object into a dict
token_response_dict = token_response_instance.to_dict()
# create an instance of TokenResponse from a dict
token_response_from_dict = TokenResponse.from_dict(token_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


