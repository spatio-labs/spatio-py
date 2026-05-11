# UpdateRowRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cells** | **Dict[str, object]** | Sparse update. Keys present in the map overwrite that column; keys absent are preserved.  | 

## Example

```python
from spatio.models.update_row_request import UpdateRowRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateRowRequest from a JSON string
update_row_request_instance = UpdateRowRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateRowRequest.to_json())

# convert the object into a dict
update_row_request_dict = update_row_request_instance.to_dict()
# create an instance of UpdateRowRequest from a dict
update_row_request_from_dict = UpdateRowRequest.from_dict(update_row_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


