# UpdateRecordTypeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**name_plural** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**attribute_schema** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.update_record_type_request import UpdateRecordTypeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRecordTypeRequest from a JSON string
update_record_type_request_instance = UpdateRecordTypeRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRecordTypeRequest.to_json())

# convert the object into a dict
update_record_type_request_dict = update_record_type_request_instance.to_dict()
# create an instance of UpdateRecordTypeRequest from a dict
update_record_type_request_from_dict = UpdateRecordTypeRequest.from_dict(update_record_type_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


