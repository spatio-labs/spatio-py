# CreateSheetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**data** | **Dict[str, object]** |  | [optional] 
**row_count** | **int** |  | [optional] 
**column_count** | **int** |  | [optional] 
**account_id** | **str** | Optional override for the target connected account. May also be passed as &#x60;?accountId&#x3D;&#x60;.  | [optional] 
**provider** | **str** |  | [optional] 

## Example

```python
from spatio.models.create_sheet_request import CreateSheetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSheetRequest from a JSON string
create_sheet_request_instance = CreateSheetRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSheetRequest.to_json())

# convert the object into a dict
create_sheet_request_dict = create_sheet_request_instance.to_dict()
# create an instance of CreateSheetRequest from a dict
create_sheet_request_from_dict = CreateSheetRequest.from_dict(create_sheet_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


