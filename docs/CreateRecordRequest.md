# CreateRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization_id** | **str** |  | [optional] 
**record_type_id** | **str** |  | 
**name** | **str** |  | [optional] 
**attributes** | **Dict[str, object]** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.create_record_request import CreateRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRecordRequest from a JSON string
create_record_request_instance = CreateRecordRequest.from_json(json)
# print the JSON string representation of the object
print(CreateRecordRequest.to_json())

# convert the object into a dict
create_record_request_dict = create_record_request_instance.to_dict()
# create an instance of CreateRecordRequest from a dict
create_record_request_from_dict = CreateRecordRequest.from_dict(create_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


