# SpatioConnection

OAuth/native integration descriptor. Open shape — categories add provider-specific capability flags. Treat unknown fields as additive. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**name** | **str** |  | [optional] 
**category** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**auth_type** | **str** |  | [optional] 
**connected** | **bool** |  | [optional] 
**connected_accounts** | **List[Dict[str, object]]** |  | [optional] 
**capabilities** | **Dict[str, object]** |  | [optional] 
**gradient_from** | **str** |  | [optional] 
**gradient_to** | **str** |  | [optional] 
**icon** | **str** |  | [optional] 

## Example

```python
from spatio.models.spatio_connection import SpatioConnection

# TODO update the JSON string below
json = "{}"
# create an instance of SpatioConnection from a JSON string
spatio_connection_instance = SpatioConnection.from_json(json)
# print the JSON string representation of the object
print(SpatioConnection.to_json())

# convert the object into a dict
spatio_connection_dict = spatio_connection_instance.to_dict()
# create an instance of SpatioConnection from a dict
spatio_connection_from_dict = SpatioConnection.from_dict(spatio_connection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


