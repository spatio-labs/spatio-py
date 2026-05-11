# CreatePresentationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**theme** | **str** |  | [optional] 
**account_id** | **str** |  | [optional] 
**provider** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_presentation_request import CreatePresentationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePresentationRequest from a JSON string
create_presentation_request_instance = CreatePresentationRequest.from_json(json)
# print the JSON string representation of the object
print(CreatePresentationRequest.to_json())

# convert the object into a dict
create_presentation_request_dict = create_presentation_request_instance.to_dict()
# create an instance of CreatePresentationRequest from a dict
create_presentation_request_from_dict = CreatePresentationRequest.from_dict(create_presentation_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


