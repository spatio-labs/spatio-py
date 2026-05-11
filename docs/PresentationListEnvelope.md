# PresentationListEnvelope


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Presentation]**](Presentation.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.presentation_list_envelope import PresentationListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of PresentationListEnvelope from a JSON string
presentation_list_envelope_instance = PresentationListEnvelope.from_json(json)
# print the JSON string representation of the object
print(PresentationListEnvelope.to_json())

# convert the object into a dict
presentation_list_envelope_dict = presentation_list_envelope_instance.to_dict()
# create an instance of PresentationListEnvelope from a dict
presentation_list_envelope_from_dict = PresentationListEnvelope.from_dict(presentation_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


