# ConnectedAppsListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[ConnectedAppItem]**](ConnectedAppItem.md) |  | 

## Example

```python
from spatio.models.connected_apps_list_response import ConnectedAppsListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectedAppsListResponse from a JSON string
connected_apps_list_response_instance = ConnectedAppsListResponse.from_json(json)
# print the JSON string representation of the object
print(ConnectedAppsListResponse.to_json())

# convert the object into a dict
connected_apps_list_response_dict = connected_apps_list_response_instance.to_dict()
# create an instance of ConnectedAppsListResponse from a dict
connected_apps_list_response_from_dict = ConnectedAppsListResponse.from_dict(connected_apps_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


