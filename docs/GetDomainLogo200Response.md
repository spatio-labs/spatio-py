# GetDomainLogo200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **str** |  | 
**logo_url** | **str** |  | 

## Example

```python
from spatio.models.get_domain_logo200_response import GetDomainLogo200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetDomainLogo200Response from a JSON string
get_domain_logo200_response_instance = GetDomainLogo200Response.from_json(json)
# print the JSON string representation of the object
print(GetDomainLogo200Response.to_json())

# convert the object into a dict
get_domain_logo200_response_dict = get_domain_logo200_response_instance.to_dict()
# create an instance of GetDomainLogo200Response from a dict
get_domain_logo200_response_from_dict = GetDomainLogo200Response.from_dict(get_domain_logo200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


