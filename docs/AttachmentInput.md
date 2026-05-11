# AttachmentInput

Inline attachment payload for `send`, `reply`, and draft requests. `data` is the raw bytes base64-encoded by the JSON encoder. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**filename** | **str** |  | 
**content_type** | **str** |  | 
**data** | **bytes** | Base64-encoded bytes. | 
**size** | **int** |  | [optional] 

## Example

```python
from spatio.models.attachment_input import AttachmentInput

# TODO update the JSON string below
json = "{}"
# create an instance of AttachmentInput from a JSON string
attachment_input_instance = AttachmentInput.from_json(json)
# print the JSON string representation of the object
print(AttachmentInput.to_json())

# convert the object into a dict
attachment_input_dict = attachment_input_instance.to_dict()
# create an instance of AttachmentInput from a dict
attachment_input_from_dict = AttachmentInput.from_dict(attachment_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


