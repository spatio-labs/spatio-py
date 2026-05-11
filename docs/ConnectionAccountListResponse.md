# ConnectionAccountListResponse

`GET /v1/connections/user` returns `{connections, user_id}` (the per-provider connected-account list). Schema kept open pending a normalize-to-`accounts` migration. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connections** | **List[Dict[str, object]]** |  | [optional] 
**user_id** | **str** |  | [optional] 
**accounts** | **List[Dict[str, object]]** |  | [optional] 

## Example

```python
from spatio.models.connection_account_list_response import ConnectionAccountListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of ConnectionAccountListResponse from a JSON string
connection_account_list_response_instance = ConnectionAccountListResponse.from_json(json)
# print the JSON string representation of the object
print(ConnectionAccountListResponse.to_json())

# convert the object into a dict
connection_account_list_response_dict = connection_account_list_response_instance.to_dict()
# create an instance of ConnectionAccountListResponse from a dict
connection_account_list_response_from_dict = ConnectionAccountListResponse.from_dict(connection_account_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


