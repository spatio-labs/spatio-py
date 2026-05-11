# ShareSettings

Public share configuration for a note. Owner-only mutation; unauthenticated readers consume `GET /public/notes/{token}` instead. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**is_public** | **bool** |  | 
**has_password** | **bool** |  | 
**share_token** | **str** | Opaque token embedded in the public URL. Empty when &#x60;isPublic&#x60; is false.  | [optional] 
**share_url** | **str** | Fully-qualified public viewer URL. Computed server-side from &#x60;PUBLIC_VIEWER_BASE&#x60; (defaults to &#x60;https://spatio.app&#x60;) and the share token. Empty when the note is private.  | [optional] 
**password_set_at** | **datetime** | When the current password was set, if any. | [optional] 

## Example

```python
from spatio.models.share_settings import ShareSettings

# TODO update the JSON string below
json = "{}"
# create an instance of ShareSettings from a JSON string
share_settings_instance = ShareSettings.from_json(json)
# print the JSON string representation of the object
print(ShareSettings.to_json())

# convert the object into a dict
share_settings_dict = share_settings_instance.to_dict()
# create an instance of ShareSettings from a dict
share_settings_from_dict = ShareSettings.from_dict(share_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


