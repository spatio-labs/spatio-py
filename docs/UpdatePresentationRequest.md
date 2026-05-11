# UpdatePresentationRequest

Partial update — every field optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**theme** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_presentation_request import UpdatePresentationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePresentationRequest from a JSON string
update_presentation_request_instance = UpdatePresentationRequest.from_json(json)
# print the JSON string representation of the object
print(UpdatePresentationRequest.to_json())

# convert the object into a dict
update_presentation_request_dict = update_presentation_request_instance.to_dict()
# create an instance of UpdatePresentationRequest from a dict
update_presentation_request_from_dict = UpdatePresentationRequest.from_dict(update_presentation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


