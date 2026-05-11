# RecordTypeListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**record_types** | [**List[RecordType]**](RecordType.md) |  | 

## Example

```python
from spatio.models.record_type_list_response import RecordTypeListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecordTypeListResponse from a JSON string
record_type_list_response_instance = RecordTypeListResponse.from_json(json)
# print the JSON string representation of the object
print(RecordTypeListResponse.to_json())

# convert the object into a dict
record_type_list_response_dict = record_type_list_response_instance.to_dict()
# create an instance of RecordTypeListResponse from a dict
record_type_list_response_from_dict = RecordTypeListResponse.from_dict(record_type_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


