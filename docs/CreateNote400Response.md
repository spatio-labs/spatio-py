# CreateNote400Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **str** | Human-readable error message. | 
**code** | **str** | Machine-readable error code. Stable across releases for the canonical codes (&#x60;ambiguous_account&#x60;, &#x60;no_notes_provider&#x60;, &#x60;note_not_found&#x60;). Absent for generic errors.  | [optional] 
**accounts** | [**List[AccountChoice]**](AccountChoice.md) |  | [optional] 

## Example

```python
from spatio.models.create_note400_response import CreateNote400Response

# TODO update the JSON string below
json = "{}"
# create an instance of CreateNote400Response from a JSON string
create_note400_response_instance = CreateNote400Response.from_json(json)
# print the JSON string representation of the object
print(CreateNote400Response.to_json())

# convert the object into a dict
create_note400_response_dict = create_note400_response_instance.to_dict()
# create an instance of CreateNote400Response from a dict
create_note400_response_from_dict = CreateNote400Response.from_dict(create_note400_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


