# CalendarAccountError


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | 
**account_name** | **str** |  | 
**error_code** | **str** |  | 
**error_message** | **str** |  | 

## Example

```python
from spatio.models.calendar_account_error import CalendarAccountError

# TODO update the JSON string below
json = "{}"
# create an instance of CalendarAccountError from a JSON string
calendar_account_error_instance = CalendarAccountError.from_json(json)
# print the JSON string representation of the object
print(CalendarAccountError.to_json())

# convert the object into a dict
calendar_account_error_dict = calendar_account_error_instance.to_dict()
# create an instance of CalendarAccountError from a dict
calendar_account_error_from_dict = CalendarAccountError.from_dict(calendar_account_error_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


