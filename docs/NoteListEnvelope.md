# NoteListEnvelope

Standard fan-out response for `GET /v1/notes`. Items aggregate notes across every connected account that contributed to the call; each contributing account contributes one `accounts[]` entry — including failed accounts, so the client can render which providers contributed and which errored without the call itself failing. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Note]**](Note.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.note_list_envelope import NoteListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of NoteListEnvelope from a JSON string
note_list_envelope_instance = NoteListEnvelope.from_json(json)
# print the JSON string representation of the object
print(NoteListEnvelope.to_json())

# convert the object into a dict
note_list_envelope_dict = note_list_envelope_instance.to_dict()
# create an instance of NoteListEnvelope from a dict
note_list_envelope_from_dict = NoteListEnvelope.from_dict(note_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


