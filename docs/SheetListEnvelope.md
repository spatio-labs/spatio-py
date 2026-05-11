# SheetListEnvelope

Fan-out response for `GET /v1/sheets`. `items` aggregates sheets across every connected account; `accounts` carries one row per contributing connection — including failures. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**items** | [**List[Sheet]**](Sheet.md) |  | 
**accounts** | [**List[AccountStatus]**](AccountStatus.md) |  | 

## Example

```python
from spatio.models.sheet_list_envelope import SheetListEnvelope

# TODO update the JSON string below
json = "{}"
# create an instance of SheetListEnvelope from a JSON string
sheet_list_envelope_instance = SheetListEnvelope.from_json(json)
# print the JSON string representation of the object
print(SheetListEnvelope.to_json())

# convert the object into a dict
sheet_list_envelope_dict = sheet_list_envelope_instance.to_dict()
# create an instance of SheetListEnvelope from a dict
sheet_list_envelope_from_dict = SheetListEnvelope.from_dict(sheet_list_envelope_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


