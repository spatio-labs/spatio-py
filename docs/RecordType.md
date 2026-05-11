# RecordType

Org-scoped record-type definition. `attribute_schema` defines the per-record attributes; treated as opaque here. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**organization_id** | **str** |  | 
**slug** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**name_plural** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 
**attribute_schema** | **List[Dict[str, object]]** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.record_type import RecordType

# TODO update the JSON string below
json = "{}"
# create an instance of RecordType from a JSON string
record_type_instance = RecordType.from_json(json)
# print the JSON string representation of the object
print(RecordType.to_json())

# convert the object into a dict
record_type_dict = record_type_instance.to_dict()
# create an instance of RecordType from a dict
record_type_from_dict = RecordType.from_dict(record_type_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


