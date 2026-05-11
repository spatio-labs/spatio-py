# CalendarProviderInfo

Metadata about one registered calendar provider.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Stable provider id (e.g. &#x60;google-calendar&#x60;, &#x60;native-calendar&#x60;). | 
**name** | **str** |  | 
**display_name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**is_system** | **bool** | &#x60;true&#x60; for built-in providers (the native calendar). | [optional] 

## Example

```python
from spatio.models.calendar_provider_info import CalendarProviderInfo

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarProviderInfo from a JSON string
calendar_provider_info_instance = CalendarProviderInfo.from_json(json)
# print the JSON string representation of the object
print(CalendarProviderInfo.to_json())

# convert the object into a dict
calendar_provider_info_dict = calendar_provider_info_instance.to_dict()
# create an instance of CalendarProviderInfo from a dict
calendar_provider_info_from_dict = CalendarProviderInfo.from_dict(calendar_provider_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


