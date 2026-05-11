# FederatedSearchRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**query** | **str** |  | 
**platforms** | **List[str]** | Subset to fan out to. Empty means all available platforms. | [optional] 
**limit** | **int** |  | [optional] [default to 25]
**page_tokens** | **Dict[str, str]** | Per-platform cursor for pagination. | [optional] 
**workspace_id** | **str** |  | [optional] 
**organization_id** | **str** |  | [optional] 
**include_shared** | **bool** |  | [optional] 
**include_archived** | **bool** |  | [optional] 

## Example

```python
from spatio.models.federated_search_request import FederatedSearchRequest

# TODO update the JSON string below
json = "{}"
# create an instance of FederatedSearchRequest from a JSON string
federated_search_request_instance = FederatedSearchRequest.from_json(json)
# print the JSON string representation of the object
print(FederatedSearchRequest.to_json())

# convert the object into a dict
federated_search_request_dict = federated_search_request_instance.to_dict()
# create an instance of FederatedSearchRequest from a dict
federated_search_request_from_dict = FederatedSearchRequest.from_dict(federated_search_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


