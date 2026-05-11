# Note

A markdown note. Notes belong to exactly one connected account (`accountId` + `provider`). The native provider stores notes in the Spatio database; external providers (Notion, Google Keep, etc.) store them upstream and round-trip through Spatio. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Stable provider id for the note. | 
**provider** | **str** | Registered provider id (e.g. &#x60;native-notes&#x60;). | [optional] 
**account_id** | **str** | Connected-account row this note belongs to. | [optional] 
**owner_user_id** | **str** | User id of the note&#39;s owner. Surfaced so the renderer can show \&quot;Shared with you\&quot; when &#x60;ownerUserId&#x60; differs from the viewer&#39;s id. Empty for non-native providers.  | [optional] 
**title** | **str** |  | 
**content** | **str** | Markdown body. The block tree at &#x60;/v1/notes/{id}/blocks&#x60; is the canonical structured representation; &#x60;content&#x60; is a flattened markdown view kept for clients that don&#39;t render blocks.  | 
**icon** | **str** | Emoji or short string used as the note&#39;s icon. | [optional] 
**cover_image** | **str** | URL of the note&#39;s cover image. | [optional] 
**parent_id** | **str** | Parent note id when notes are nested. | [optional] 
**properties** | **Dict[str, object]** | Free-form provider-specific properties (tags, etc.). | [optional] 
**archived** | **bool** |  | 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**last_edited_by** | **str** | User id of the most recent editor. | [optional] 

## Example

```python
from spatio.models.note import Note

# TODO update the JSON string below
json = "{}"
# create an instance of Note from a JSON string
note_instance = Note.from_json(json)
# print the JSON string representation of the object
print(Note.to_json())

# convert the object into a dict
note_dict = note_instance.to_dict()
# create an instance of Note from a dict
note_from_dict = Note.from_dict(note_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


