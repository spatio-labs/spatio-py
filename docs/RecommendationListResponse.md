# RecommendationListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Recommendation]**](Recommendation.md) |  | 

## Example

```python
from spatio.models.recommendation_list_response import RecommendationListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecommendationListResponse from a JSON string
recommendation_list_response_instance = RecommendationListResponse.from_json(json)
# print the JSON string representation of the object
print(RecommendationListResponse.to_json())

# convert the object into a dict
recommendation_list_response_dict = recommendation_list_response_instance.to_dict()
# create an instance of RecommendationListResponse from a dict
recommendation_list_response_from_dict = RecommendationListResponse.from_dict(recommendation_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


