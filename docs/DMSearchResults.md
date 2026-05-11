# DMSearchResults


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | **object** | Provider-shaped search results. Treat as opaque. | [optional] 

## Example

```python
from spatio.models.dm_search_results import DMSearchResults

# TODO update the JSON string below
json = "{}"
# create an instance of DMSearchResults from a JSON string
dm_search_results_instance = DMSearchResults.from_json(json)
# print the JSON string representation of the object
print(DMSearchResults.to_json())

# convert the object into a dict
dm_search_results_dict = dm_search_results_instance.to_dict()
# create an instance of DMSearchResults from a dict
dm_search_results_from_dict = DMSearchResults.from_dict(dm_search_results_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


