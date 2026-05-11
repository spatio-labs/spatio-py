# UpdateBlockRequest

Partial update — only fields present in the body are touched.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | [**BlockContent**](BlockContent.md) |  | [optional] 
**properties** | **Dict[str, object]** |  | [optional] 
**archived** | **bool** |  | [optional] 

## Example

```python
from spatio.models.update_block_request import UpdateBlockRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateBlockRequest from a JSON string
update_block_request_instance = UpdateBlockRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateBlockRequest.to_json())

# convert the object into a dict
update_block_request_dict = update_block_request_instance.to_dict()
# create an instance of UpdateBlockRequest from a dict
update_block_request_from_dict = UpdateBlockRequest.from_dict(update_block_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


