# CreateLabelRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**message_list_visibility** | **str** |  | [optional] 
**label_list_visibility** | **str** |  | [optional] 
**color** | [**LabelColor**](LabelColor.md) |  | [optional] 

## Example

```python
from spatio.models.create_label_request import CreateLabelRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateLabelRequest from a JSON string
create_label_request_instance = CreateLabelRequest.from_json(json)
# print the JSON string representation of the object
print(CreateLabelRequest.to_json())

# convert the object into a dict
create_label_request_dict = create_label_request_instance.to_dict()
# create an instance of CreateLabelRequest from a dict
create_label_request_from_dict = CreateLabelRequest.from_dict(create_label_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


