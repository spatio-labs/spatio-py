# UpdateSheetRequest

Partial update — every field is optional.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**data** | **Dict[str, object]** |  | [optional] 
**row_count** | **int** |  | [optional] 
**column_count** | **int** |  | [optional] 
**is_public** | **bool** |  | [optional] 
**is_read_only** | **bool** |  | [optional] 

## Example

```python
from spatio.models.update_sheet_request import UpdateSheetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSheetRequest from a JSON string
update_sheet_request_instance = UpdateSheetRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateSheetRequest.to_json())

# convert the object into a dict
update_sheet_request_dict = update_sheet_request_instance.to_dict()
# create an instance of UpdateSheetRequest from a dict
update_sheet_request_from_dict = UpdateSheetRequest.from_dict(update_sheet_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


