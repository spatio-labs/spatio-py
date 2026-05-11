# RichTextObject


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**text** | **str** |  | [optional] 
**annotations** | [**TextAnnotations**](TextAnnotations.md) |  | [optional] 
**href** | **str** | External URL (&#x60;https://…&#x60;) or internal note anchor (&#x60;#blockId&#x60;, &#x60;#heading-slug&#x60;). Internal anchors resolve to the matching block in the same note.  | [optional] 

## Example

```python
from spatio.models.rich_text_object import RichTextObject

# TODO update the JSON string below
json = "{}"
# create an instance of RichTextObject from a JSON string
rich_text_object_instance = RichTextObject.from_json(json)
# print the JSON string representation of the object
print(RichTextObject.to_json())

# convert the object into a dict
rich_text_object_dict = rich_text_object_instance.to_dict()
# create an instance of RichTextObject from a dict
rich_text_object_from_dict = RichTextObject.from_dict(rich_text_object_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


