# FederatedSearch200ResponseItemsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**entity_type** | **str** |  | [optional] 
**platform** | **str** |  | [optional] 
**provider_id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**snippet** | **str** |  | [optional] 
**author** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**score** | **float** |  | [optional] 

## Example

```python
from spatio.models.federated_search200_response_items_inner import FederatedSearch200ResponseItemsInner

# TODO update the JSON string below
json = "{}"
# create an instance of FederatedSearch200ResponseItemsInner from a JSON string
federated_search200_response_items_inner_instance = FederatedSearch200ResponseItemsInner.from_json(json)
# print the JSON string representation of the object
print(FederatedSearch200ResponseItemsInner.to_json())

# convert the object into a dict
federated_search200_response_items_inner_dict = federated_search200_response_items_inner_instance.to_dict()
# create an instance of FederatedSearch200ResponseItemsInner from a dict
federated_search200_response_items_inner_from_dict = FederatedSearch200ResponseItemsInner.from_dict(federated_search200_response_items_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


