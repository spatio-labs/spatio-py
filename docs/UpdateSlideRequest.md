# UpdateSlideRequest

Partial update — every field optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**notes** | **str** |  | [optional] 
**layout** | **str** |  | [optional] 
**background_color** | **str** |  | [optional] 
**background_image_url** | **str** |  | [optional] 
**text_color** | **str** |  | [optional] 
**transition** | **str** |  | [optional] 
**position** | **int** |  | [optional] 

## Example

```python
from spatio.models.update_slide_request import UpdateSlideRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSlideRequest from a JSON string
update_slide_request_instance = UpdateSlideRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateSlideRequest.to_json())

# convert the object into a dict
update_slide_request_dict = update_slide_request_instance.to_dict()
# create an instance of UpdateSlideRequest from a dict
update_slide_request_from_dict = UpdateSlideRequest.from_dict(update_slide_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


