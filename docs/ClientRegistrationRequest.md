# ClientRegistrationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_name** | **str** |  | 
**redirect_uris** | **List[str]** |  | 
**grant_types** | **List[str]** |  | [optional] [default to ["authorization_code","refresh_token"]]
**response_types** | **List[str]** |  | [optional] [default to ["code"]]
**scope** | **str** | Space-separated scope list. Defaults to &#x60;read:*&#x60;. | [optional] 
**token_endpoint_auth_method** | **str** |  | [optional] [default to 'none']
**client_uri** | **str** |  | [optional] 
**logo_uri** | **str** |  | [optional] 
**policy_uri** | **str** |  | [optional] 
**tos_uri** | **str** |  | [optional] 

## Example

```python
from spatio.models.client_registration_request import ClientRegistrationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ClientRegistrationRequest from a JSON string
client_registration_request_instance = ClientRegistrationRequest.from_json(json)
# print the JSON string representation of the object
print(ClientRegistrationRequest.to_json())

# convert the object into a dict
client_registration_request_dict = client_registration_request_instance.to_dict()
# create an instance of ClientRegistrationRequest from a dict
client_registration_request_from_dict = ClientRegistrationRequest.from_dict(client_registration_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


