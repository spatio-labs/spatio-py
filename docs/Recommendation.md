# Recommendation

Agent-authored proposal that surfaces on the home feed. Status transitions: `pending` → `accepted | dismissed | expired`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**workspace_id** | **str** |  | [optional] 
**user_id** | **str** |  | [optional] 
**kind** | **str** | Provider-tagged proposal kind (e.g. &#x60;note.draft&#x60;, &#x60;task.followup&#x60;). | [optional] 
**title** | **str** |  | [optional] 
**body** | **str** |  | [optional] 
**status** | **str** |  | 
**payload** | **Dict[str, object]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.recommendation import Recommendation

# TODO update the JSON string below
json = "{}"
# create an instance of Recommendation from a JSON string
recommendation_instance = Recommendation.from_json(json)
# print the JSON string representation of the object
print(Recommendation.to_json())

# convert the object into a dict
recommendation_dict = recommendation_instance.to_dict()
# create an instance of Recommendation from a dict
recommendation_from_dict = Recommendation.from_dict(recommendation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


