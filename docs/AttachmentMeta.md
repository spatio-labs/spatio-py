# AttachmentMeta

Attachment metadata; binary fetched via the attachment endpoint.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**filename** | **str** |  | 
**content_type** | **str** |  | 
**size** | **int** |  | 

## Example

```python
from spatio.models.attachment_meta import AttachmentMeta

# TODO update the JSON string below
json = "{}"
# create an instance of AttachmentMeta from a JSON string
attachment_meta_instance = AttachmentMeta.from_json(json)
# print the JSON string representation of the object
print(AttachmentMeta.to_json())

# convert the object into a dict
attachment_meta_dict = attachment_meta_instance.to_dict()
# create an instance of AttachmentMeta from a dict
attachment_meta_from_dict = AttachmentMeta.from_dict(attachment_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


