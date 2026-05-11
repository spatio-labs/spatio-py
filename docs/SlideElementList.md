# SlideElementList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**elements** | [**List[SlideElement]**](SlideElement.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.slide_element_list import SlideElementList

# TODO update the JSON string below
json = "{}"
# create an instance of SlideElementList from a JSON string
slide_element_list_instance = SlideElementList.from_json(json)
# print the JSON string representation of the object
print(SlideElementList.to_json())

# convert the object into a dict
slide_element_list_dict = slide_element_list_instance.to_dict()
# create an instance of SlideElementList from a dict
slide_element_list_from_dict = SlideElementList.from_dict(slide_element_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


