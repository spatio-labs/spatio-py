# CreatePATResponse

The full token (prefix + secret) is returned ONLY on creation. Store it now or you'll have to recreate; the API never returns the secret again. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**token** | **str** |  | 
**pat** | [**PersonalAccessToken**](PersonalAccessToken.md) |  | [optional] 

## Example

```python
from spatio.models.create_pat_response import CreatePATResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePATResponse from a JSON string
create_pat_response_instance = CreatePATResponse.from_json(json)
# print the JSON string representation of the object
print(CreatePATResponse.to_json())

# convert the object into a dict
create_pat_response_dict = create_pat_response_instance.to_dict()
# create an instance of CreatePATResponse from a dict
create_pat_response_from_dict = CreatePATResponse.from_dict(create_pat_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


