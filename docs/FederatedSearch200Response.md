# FederatedSearch200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[FederatedSearch200ResponseItemsInner]**](FederatedSearch200ResponseItemsInner.md) |  | 
**next_page_tokens** | **Dict[str, str]** |  | [optional] 
**per_platform** | [**Dict[str, FederatedSearch200ResponsePerPlatformValue]**](FederatedSearch200ResponsePerPlatformValue.md) |  | 
**errors** | **Dict[str, str]** | Per-platform errors. Other platforms still return results. | [optional] 
**total_returned** | **int** |  | 
**took** | **str** | Aggregate wall-clock time for the fan-out, e.g. \&quot;120ms\&quot;. | 

## Example

```python
from spatio.models.federated_search200_response import FederatedSearch200Response

# TODO update the JSON string below
json = "{}"
# create an instance of FederatedSearch200Response from a JSON string
federated_search200_response_instance = FederatedSearch200Response.from_json(json)
# print the JSON string representation of the object
print(FederatedSearch200Response.to_json())

# convert the object into a dict
federated_search200_response_dict = federated_search200_response_instance.to_dict()
# create an instance of FederatedSearch200Response from a dict
federated_search200_response_from_dict = FederatedSearch200Response.from_dict(federated_search200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


