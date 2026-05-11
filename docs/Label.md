# Label


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | 
**type** | **str** | Provider-specific label type. Common values: &#x60;system&#x60;, &#x60;user&#x60;. Not enumerated to avoid forcing a breaking change every time a provider adds one.  | 
**message_list_visibility** | **str** |  | [optional] 
**label_list_visibility** | **str** |  | [optional] 
**color** | [**LabelColor**](LabelColor.md) |  | [optional] 

## Example

```python
from spatio.models.label import Label

# TODO update the JSON string below
json = "{}"
# create an instance of Label from a JSON string
label_instance = Label.from_json(json)
# print the JSON string representation of the object
print(Label.to_json())

# convert the object into a dict
label_dict = label_instance.to_dict()
# create an instance of Label from a dict
label_from_dict = Label.from_dict(label_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


