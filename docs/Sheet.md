# Sheet

A spreadsheet. Sheets belong to exactly one connected account (`accountId` + `provider`). The native provider stores sheets in the Spatio database; external providers (Google Sheets, Excel Online, etc.) round-trip through Spatio.  `data` is a free-form bag for provider-specific blobs (cell matrices, formulas, formatting). Clients that walk rows / cells should use the dedicated row + cell endpoints; `data` is only meaningful when round-tripping with an external provider that embeds its native format here. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** | Registered provider id (e.g. &#x60;native-sheets&#x60;). | [optional] 
**account_id** | **str** | Connected-account row this sheet belongs to. | [optional] 
**owner_user_id** | **str** | User id of the sheet owner; non-native providers leave empty. | [optional] 
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**data** | **Dict[str, object]** | Free-form provider blob. Treat as opaque. | [optional] 
**row_count** | **int** |  | 
**column_count** | **int** |  | 
**sheet_count** | **int** | Tab count when the file contains multiple sheets. | 
**is_public** | **bool** |  | 
**is_read_only** | **bool** |  | 
**file_size** | **int** |  | [optional] 
**last_accessed_at** | **datetime** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.sheet import Sheet

# TODO update the JSON string below
json = "{}"
# create an instance of Sheet from a JSON string
sheet_instance = Sheet.from_json(json)
# print the JSON string representation of the object
print(Sheet.to_json())

# convert the object into a dict
sheet_dict = sheet_instance.to_dict()
# create an instance of Sheet from a dict
sheet_from_dict = Sheet.from_dict(sheet_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


