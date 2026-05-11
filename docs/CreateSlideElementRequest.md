# CreateSlideElementRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**element_type** | **str** |  | 
**content** | **Dict[str, object]** |  | [optional] 
**x** | **float** |  | [optional] 
**y** | **float** |  | [optional] 
**width** | **float** |  | [optional] 
**height** | **float** |  | [optional] 
**rotation** | **float** |  | [optional] 
**z_index** | **int** |  | [optional] 

## Example

```python
from spatio.models.create_slide_element_request import CreateSlideElementRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSlideElementRequest from a JSON string
create_slide_element_request_instance = CreateSlideElementRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSlideElementRequest.to_json())

# convert the object into a dict
create_slide_element_request_dict = create_slide_element_request_instance.to_dict()
# create an instance of CreateSlideElementRequest from a dict
create_slide_element_request_from_dict = CreateSlideElementRequest.from_dict(create_slide_element_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


