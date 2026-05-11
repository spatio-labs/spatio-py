# ClientRegistrationResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**client_id** | **str** |  | 
**client_secret** | **str** | Only returned when token_endpoint_auth_method is client_secret_*. | [optional] 
**client_name** | **str** |  | 
**redirect_uris** | **List[str]** |  | 
**grant_types** | **List[str]** |  | [optional] 
**response_types** | **List[str]** |  | [optional] 
**scope** | **str** |  | [optional] 
**token_endpoint_auth_method** | **str** |  | [optional] 
**registration_access_token** | **str** |  | 
**registration_client_uri** | **str** |  | [optional] 
**client_id_issued_at** | **int** |  | 

## Example

```python
from spatio.models.client_registration_response import ClientRegistrationResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ClientRegistrationResponse from a JSON string
client_registration_response_instance = ClientRegistrationResponse.from_json(json)
# print the JSON string representation of the object
print(ClientRegistrationResponse.to_json())

# convert the object into a dict
client_registration_response_dict = client_registration_response_instance.to_dict()
# create an instance of ClientRegistrationResponse from a dict
client_registration_response_from_dict = ClientRegistrationResponse.from_dict(client_registration_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


