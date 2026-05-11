# UpdateSlideElementRequest

Partial update — every field optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**element_type** | **str** |  | [optional] 
**content** | **Dict[str, object]** |  | [optional] 
**x** | **float** |  | [optional] 
**y** | **float** |  | [optional] 
**width** | **float** |  | [optional] 
**height** | **float** |  | [optional] 
**rotation** | **float** |  | [optional] 
**z_index** | **int** |  | [optional] 

## Example

```python
from spatio.models.update_slide_element_request import UpdateSlideElementRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSlideElementRequest from a JSON string
update_slide_element_request_instance = UpdateSlideElementRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateSlideElementRequest.to_json())

# convert the object into a dict
update_slide_element_request_dict = update_slide_element_request_instance.to_dict()
# create an instance of UpdateSlideElementRequest from a dict
update_slide_element_request_from_dict = UpdateSlideElementRequest.from_dict(update_slide_element_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


