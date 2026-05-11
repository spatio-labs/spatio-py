# DisconnectConnectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connection_id** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.disconnect_connection_request import DisconnectConnectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DisconnectConnectionRequest from a JSON string
disconnect_connection_request_instance = DisconnectConnectionRequest.from_json(json)
# print the JSON string representation of the object
print(DisconnectConnectionRequest.to_json())

# convert the object into a dict
disconnect_connection_request_dict = disconnect_connection_request_instance.to_dict()
# create an instance of DisconnectConnectionRequest from a dict
disconnect_connection_request_from_dict = DisconnectConnectionRequest.from_dict(disconnect_connection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


