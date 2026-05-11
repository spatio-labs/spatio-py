# PATScopesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**scopes** | **List[str]** |  | 

## Example

```python
from spatio.models.pat_scopes_response import PATScopesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PATScopesResponse from a JSON string
pat_scopes_response_instance = PATScopesResponse.from_json(json)
# print the JSON string representation of the object
print(PATScopesResponse.to_json())

# convert the object into a dict
pat_scopes_response_dict = pat_scopes_response_instance.to_dict()
# create an instance of PATScopesResponse from a dict
pat_scopes_response_from_dict = PATScopesResponse.from_dict(pat_scopes_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


