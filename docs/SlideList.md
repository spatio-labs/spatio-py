# SlideList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slides** | [**List[Slide]**](Slide.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.slide_list import SlideList

# TODO update the JSON string below
json = "{}"
# create an instance of SlideList from a JSON string
slide_list_instance = SlideList.from_json(json)
# print the JSON string representation of the object
print(SlideList.to_json())

# convert the object into a dict
slide_list_dict = slide_list_instance.to_dict()
# create an instance of SlideList from a dict
slide_list_from_dict = SlideList.from_dict(slide_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


