# CreateNoteRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | 
**content** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**cover_image** | **str** |  | [optional] 
**parent_id** | **str** |  | [optional] 
**properties** | **Dict[str, object]** |  | [optional] 
**account_id** | **str** | Optional override for the target connected account. May also be passed as a &#x60;?accountId&#x3D;&#x60; query param.  | [optional] 
**provider** | **str** | Optional provider id (alternative to &#x60;accountId&#x60; when only one account exists for the provider). May also be passed as a &#x60;?provider&#x3D;&#x60; query param.  | [optional] 

## Example

```python
from spatio.models.create_note_request import CreateNoteRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateNoteRequest from a JSON string
create_note_request_instance = CreateNoteRequest.from_json(json)
# print the JSON string representation of the object
print(CreateNoteRequest.to_json())

# convert the object into a dict
create_note_request_dict = create_note_request_instance.to_dict()
# create an instance of CreateNoteRequest from a dict
create_note_request_from_dict = CreateNoteRequest.from_dict(create_note_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


