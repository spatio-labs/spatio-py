# UpdateRecommendationStatusRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | 

## Example

```python
from spatio.models.update_recommendation_status_request import UpdateRecommendationStatusRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRecommendationStatusRequest from a JSON string
update_recommendation_status_request_instance = UpdateRecommendationStatusRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRecommendationStatusRequest.to_json())

# convert the object into a dict
update_recommendation_status_request_dict = update_recommendation_status_request_instance.to_dict()
# create an instance of UpdateRecommendationStatusRequest from a dict
update_recommendation_status_request_from_dict = UpdateRecommendationStatusRequest.from_dict(update_recommendation_status_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


