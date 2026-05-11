# CreateRecordTypeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**organization_id** | **str** |  | [optional] 
**slug** | **str** |  | [optional] 
**name** | **str** |  | 
**name_plural** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**attribute_schema** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.create_record_type_request import CreateRecordTypeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateRecordTypeRequest from a JSON string
create_record_type_request_instance = CreateRecordTypeRequest.from_json(json)
# print the JSON string representation of the object
print(CreateRecordTypeRequest.to_json())

# convert the object into a dict
create_record_type_request_dict = create_record_type_request_instance.to_dict()
# create an instance of CreateRecordTypeRequest from a dict
create_record_type_request_from_dict = CreateRecordTypeRequest.from_dict(create_record_type_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


