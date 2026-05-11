# CreateSlideRequest

`presentationId` in the body is allowed but redundant when posting to `/v1/slides/{id}/slides` — the path id wins. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**presentation_id** | **str** |  | [optional] 
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
from spatio.models.create_slide_request import CreateSlideRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSlideRequest from a JSON string
create_slide_request_instance = CreateSlideRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSlideRequest.to_json())

# convert the object into a dict
create_slide_request_dict = create_slide_request_instance.to_dict()
# create an instance of CreateSlideRequest from a dict
create_slide_request_from_dict = CreateSlideRequest.from_dict(create_slide_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


