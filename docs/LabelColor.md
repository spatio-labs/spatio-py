# LabelColor


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text_color** | **str** |  | 
**background_color** | **str** |  | 

## Example

```python
from spatio.models.label_color import LabelColor

# TODO update the JSON string below
json = "{}"
# create an instance of LabelColor from a JSON string
label_color_instance = LabelColor.from_json(json)
# print the JSON string representation of the object
print(LabelColor.to_json())

# convert the object into a dict
label_color_dict = label_color_instance.to_dict()
# create an instance of LabelColor from a dict
label_color_from_dict = LabelColor.from_dict(label_color_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


