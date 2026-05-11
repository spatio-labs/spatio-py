# DMMessageEnvelope

Generic single-message wrapper used by reply/forward/attach responses. `message` is the resulting `ChatMessage`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | [**ChatMessage**](ChatMessage.md) |  | 

## Example

```python
from spatio.models.dm_message_envelope import DMMessageEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of DMMessageEnvelope from a JSON string
dm_message_envelope_instance = DMMessageEnvelope.from_json(json)
# print the JSON string representation of the object
print(DMMessageEnvelope.to_json())

# convert the object into a dict
dm_message_envelope_dict = dm_message_envelope_instance.to_dict()
# create an instance of DMMessageEnvelope from a dict
dm_message_envelope_from_dict = DMMessageEnvelope.from_dict(dm_message_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


