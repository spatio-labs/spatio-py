# SlideElement

One canvas object on a slide — text box, shape, image, etc. `content` is renderer-specific JSON (e.g. fabric.js properties: text, fill, fontSize, src). Identified by a stable `id` so MCP / agent operations stay idempotent across retries. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**slide_id** | **str** |  | 
**element_type** | **str** | Free-form type id (&#x60;text&#x60;, &#x60;image&#x60;, &#x60;shape&#x60;, etc.). | 
**content** | **Dict[str, object]** |  | 
**x** | **float** |  | 
**y** | **float** |  | 
**width** | **float** |  | 
**height** | **float** |  | 
**rotation** | **float** | Degrees. | 
**z_index** | **int** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.slide_element import SlideElement

# TODO update the JSON string below
json = "{}"
# create an instance of SlideElement from a JSON string
slide_element_instance = SlideElement.from_json(json)
# print the JSON string representation of the object
print(SlideElement.to_json())

# convert the object into a dict
slide_element_dict = slide_element_instance.to_dict()
# create an instance of SlideElement from a dict
slide_element_from_dict = SlideElement.from_dict(slide_element_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


