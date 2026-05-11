# ConnectionListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connections** | [**List[SpatioConnection]**](SpatioConnection.md) |  | 
**categories** | **List[str]** |  | [optional] 

## Example

```python
from spatio.models.connection_list_response import ConnectionListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectionListResponse from a JSON string
connection_list_response_instance = ConnectionListResponse.from_json(json)
# print the JSON string representation of the object
print(ConnectionListResponse.to_json())

# convert the object into a dict
connection_list_response_dict = connection_list_response_instance.to_dict()
# create an instance of ConnectionListResponse from a dict
connection_list_response_from_dict = ConnectionListResponse.from_dict(connection_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


