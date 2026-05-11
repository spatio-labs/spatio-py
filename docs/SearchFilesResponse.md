# SearchFilesResponse

In-memory substring search across the caller's files. Provider filtering isn't standardized across providers, so the platform lists up to ~500 files and filters locally — `total` is the pre-truncation count, not the global count. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**files** | [**List[SpatioFile]**](SpatioFile.md) |  | [optional] 
**total** | **int** |  | 
**has_more** | **bool** |  | 
**query** | **str** |  | 

## Example

```python
from spatio.models.search_files_response import SearchFilesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of SearchFilesResponse from a JSON string
search_files_response_instance = SearchFilesResponse.from_json(json)
# print the JSON string representation of the object
print(SearchFilesResponse.to_json())

# convert the object into a dict
search_files_response_dict = search_files_response_instance.to_dict()
# create an instance of SearchFilesResponse from a dict
search_files_response_from_dict = SearchFilesResponse.from_dict(search_files_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


