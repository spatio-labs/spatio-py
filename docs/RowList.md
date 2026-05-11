# RowList


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rows** | [**List[Row]**](Row.md) |  | 
**total** | **int** |  | 

## Example

```python
from spatio.models.row_list import RowList

# TODO update the JSON string below
json = "{}"
# create an instance of RowList from a JSON string
row_list_instance = RowList.from_json(json)
# print the JSON string representation of the object
print(RowList.to_json())

# convert the object into a dict
row_list_dict = row_list_instance.to_dict()
# create an instance of RowList from a dict
row_list_from_dict = RowList.from_dict(row_list_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


