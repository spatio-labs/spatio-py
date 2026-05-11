# Session


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**ip_address** | **str** |  | [optional] 
**user_agent** | **str** |  | [optional] 
**device_type** | **str** |  | [optional] 
**browser** | **str** |  | [optional] 
**os** | **str** |  | [optional] 
**country** | **str** |  | [optional] 
**city** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**last_active_at** | **datetime** |  | [optional] 
**is_current** | **bool** |  | [optional] 

## Example

```python
from spatio.models.session import Session

# TODO update the JSON string below
json = "{}"
# create an instance of Session from a JSON string
session_instance = Session.from_json(json)
# print the JSON string representation of the object
print(Session.to_json())

# convert the object into a dict
session_dict = session_instance.to_dict()
# create an instance of Session from a dict
session_from_dict = Session.from_dict(session_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


