# CalendarProvidersInfo

Registered calendar providers. Returned regardless of whether the caller has connected any. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**providers** | [**List[CalendarProviderInfo]**](CalendarProviderInfo.md) |  | 

## Example

```python
from spatio.models.calendar_providers_info import CalendarProvidersInfo

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarProvidersInfo from a JSON string
calendar_providers_info_instance = CalendarProvidersInfo.from_json(json)
# print the JSON string representation of the object
print(CalendarProvidersInfo.to_json())

# convert the object into a dict
calendar_providers_info_dict = calendar_providers_info_instance.to_dict()
# create an instance of CalendarProvidersInfo from a dict
calendar_providers_info_from_dict = CalendarProvidersInfo.from_dict(calendar_providers_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


