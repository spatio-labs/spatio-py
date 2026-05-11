# UpdateRecordRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**attributes** | **Dict[str, object]** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.update_record_request import UpdateRecordRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRecordRequest from a JSON string
update_record_request_instance = UpdateRecordRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRecordRequest.to_json())

# convert the object into a dict
update_record_request_dict = update_record_request_instance.to_dict()
# create an instance of UpdateRecordRequest from a dict
update_record_request_from_dict = UpdateRecordRequest.from_dict(update_record_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


