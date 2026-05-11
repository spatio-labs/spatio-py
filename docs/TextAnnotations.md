# TextAnnotations

Inline formatting flags for a `RichTextObject`.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**bold** | **bool** |  | 
**italic** | **bool** |  | 
**strikethrough** | **bool** |  | 
**underline** | **bool** |  | 
**code** | **bool** |  | 
**color** | **str** |  | [optional] 

## Example

```python
from spatio.models.text_annotations import TextAnnotations

# TODO update the JSON string below
json = "{}"
# create an instance of TextAnnotations from a JSON string
text_annotations_instance = TextAnnotations.from_json(json)
# print the JSON string representation of the object
print(TextAnnotations.to_json())

# convert the object into a dict
text_annotations_dict = text_annotations_instance.to_dict()
# create an instance of TextAnnotations from a dict
text_annotations_from_dict = TextAnnotations.from_dict(text_annotations_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


