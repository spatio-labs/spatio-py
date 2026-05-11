# DMReactionResponse

`reactions` shape is provider-specific; treat as opaque.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**reactions** | **object** | Updated reaction list for the message. | [optional] 

## Example

```python
from spatio.models.dm_reaction_response import DMReactionResponse

# TODO update the JSON string below
json = "{}"
# create an instance of DMReactionResponse from a JSON string
dm_reaction_response_instance = DMReactionResponse.from_json(json)
# print the JSON string representation of the object
print(DMReactionResponse.to_json())

# convert the object into a dict
dm_reaction_response_dict = dm_reaction_response_instance.to_dict()
# create an instance of DMReactionResponse from a dict
dm_reaction_response_from_dict = DMReactionResponse.from_dict(dm_reaction_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


