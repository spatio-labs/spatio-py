# DMAttachRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**kind** | **str** | Attachment kind (&#x60;image&#x60;, &#x60;file&#x60;, &#x60;audio&#x60;, &#x60;video&#x60;, etc.). | 
**url** | **str** |  | 
**filename** | **str** |  | [optional] 
**size_bytes** | **int** |  | [optional] 
**mime_type** | **str** |  | [optional] 
**thumbnail_url** | **str** |  | [optional] 
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_attach_request import DMAttachRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMAttachRequest from a JSON string
dm_attach_request_instance = DMAttachRequest.from_json(json)
# print the JSON string representation of the object
print(DMAttachRequest.to_json())

# convert the object into a dict
dm_attach_request_dict = dm_attach_request_instance.to_dict()
# create an instance of DMAttachRequest from a dict
dm_attach_request_from_dict = DMAttachRequest.from_dict(dm_attach_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


