# DMReactionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**emoji** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_reaction_request import DMReactionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMReactionRequest from a JSON string
dm_reaction_request_instance = DMReactionRequest.from_json(json)
# print the JSON string representation of the object
print(DMReactionRequest.to_json())

# convert the object into a dict
dm_reaction_request_dict = dm_reaction_request_instance.to_dict()
# create an instance of DMReactionRequest from a dict
dm_reaction_request_from_dict = DMReactionRequest.from_dict(dm_reaction_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


