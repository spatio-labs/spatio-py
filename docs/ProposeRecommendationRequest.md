# ProposeRecommendationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**workspace_id** | **str** |  | [optional] 
**kind** | **str** |  | 
**title** | **str** |  | [optional] 
**body** | **str** |  | [optional] 
**payload** | **Dict[str, object]** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.propose_recommendation_request import ProposeRecommendationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ProposeRecommendationRequest from a JSON string
propose_recommendation_request_instance = ProposeRecommendationRequest.from_json(json)
# print the JSON string representation of the object
print(ProposeRecommendationRequest.to_json())

# convert the object into a dict
propose_recommendation_request_dict = propose_recommendation_request_instance.to_dict()
# create an instance of ProposeRecommendationRequest from a dict
propose_recommendation_request_from_dict = ProposeRecommendationRequest.from_dict(propose_recommendation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


