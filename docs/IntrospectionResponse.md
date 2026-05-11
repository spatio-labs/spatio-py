# IntrospectionResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**active** | **bool** |  | 
**token_type** | **str** | &#x60;oauth&#x60; or &#x60;pat&#x60;. | [optional] 
**client_id** | **str** |  | [optional] 
**user_id** | **str** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 
**exp** | **int** |  | [optional] 

## Example

```python
from spatio.models.introspection_response import IntrospectionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of IntrospectionResponse from a JSON string
introspection_response_instance = IntrospectionResponse.from_json(json)
# print the JSON string representation of the object
print(IntrospectionResponse.to_json())

# convert the object into a dict
introspection_response_dict = introspection_response_instance.to_dict()
# create an instance of IntrospectionResponse from a dict
introspection_response_from_dict = IntrospectionResponse.from_dict(introspection_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


