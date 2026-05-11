# Presentation

A slide deck. Presentations belong to one connected account (`accountId` + `provider`). Native deck storage lives in Spatio's DB; external providers (Google Slides, etc.) round-trip. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**owner_user_id** | **str** |  | [optional] 
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**theme** | **str** | Free-form theme id; provider-specific. | [optional] 
**thumbnail_url** | **str** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**last_viewed_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.presentation import Presentation

# TODO update the JSON string below
json = "{}"
# create an instance of Presentation from a JSON string
presentation_instance = Presentation.from_json(json)
# print the JSON string representation of the object
print(Presentation.to_json())

# convert the object into a dict
presentation_dict = presentation_instance.to_dict()
# create an instance of Presentation from a dict
presentation_from_dict = Presentation.from_dict(presentation_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


