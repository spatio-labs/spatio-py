# InstallConnectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**connection_id** | **str** |  | 
**account_id** | **str** |  | [optional] 
**metadata** | **Dict[str, object]** |  | [optional] 

## Example

```python
from spatio.models.install_connection_request import InstallConnectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of InstallConnectionRequest from a JSON string
install_connection_request_instance = InstallConnectionRequest.from_json(json)
# print the JSON string representation of the object
print(InstallConnectionRequest.to_json())

# convert the object into a dict
install_connection_request_dict = install_connection_request_instance.to_dict()
# create an instance of InstallConnectionRequest from a dict
install_connection_request_from_dict = InstallConnectionRequest.from_dict(install_connection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


