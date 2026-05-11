# RefreshConnectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connection_id** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.refresh_connection_request import RefreshConnectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of RefreshConnectionRequest from a JSON string
refresh_connection_request_instance = RefreshConnectionRequest.from_json(json)
# print the JSON string representation of the object
print(RefreshConnectionRequest.to_json())

# convert the object into a dict
refresh_connection_request_dict = refresh_connection_request_instance.to_dict()
# create an instance of RefreshConnectionRequest from a dict
refresh_connection_request_from_dict = RefreshConnectionRequest.from_dict(refresh_connection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


