# RecordListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**records** | [**List[Record]**](Record.md) |  | 
**total_results** | **int** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.record_list_response import RecordListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of RecordListResponse from a JSON string
record_list_response_instance = RecordListResponse.from_json(json)
# print the JSON string representation of the object
print(RecordListResponse.to_json())

# convert the object into a dict
record_list_response_dict = record_list_response_instance.to_dict()
# create an instance of RecordListResponse from a dict
record_list_response_from_dict = RecordListResponse.from_dict(record_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


