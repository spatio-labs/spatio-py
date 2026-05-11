# PATListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tokens** | [**List[PersonalAccessToken]**](PersonalAccessToken.md) |  | 
**available_scopes** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.pat_list_response import PATListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of PATListResponse from a JSON string
pat_list_response_instance = PATListResponse.from_json(json)
# print the JSON string representation of the object
print(PATListResponse.to_json())

# convert the object into a dict
pat_list_response_dict = pat_list_response_instance.to_dict()
# create an instance of PATListResponse from a dict
pat_list_response_from_dict = PATListResponse.from_dict(pat_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


