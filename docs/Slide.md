# Slide


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**presentation_id** | **str** |  | 
**title** | **str** |  | 
**notes** | **str** | Speaker notes. | [optional] 
**layout** | **str** | Free-form layout id. Provider-specific (&#x60;title&#x60;, &#x60;two-column&#x60;, &#x60;image-left&#x60;, custom). Not enumerated to avoid forcing a breaking change every time a provider adds one.  | [optional] 
**background_color** | **str** |  | [optional] 
**background_image_url** | **str** |  | [optional] 
**text_color** | **str** |  | [optional] 
**transition** | **str** | Free-form transition id. | [optional] 
**position** | **int** | Zero-based position within the presentation. | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.slide import Slide

# TODO update the JSON string below
json = "{}"
# create an instance of Slide from a JSON string
slide_instance = Slide.from_json(json)
# print the JSON string representation of the object
print(Slide.to_json())

# convert the object into a dict
slide_dict = slide_instance.to_dict()
# create an instance of Slide from a dict
slide_from_dict = Slide.from_dict(slide_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


