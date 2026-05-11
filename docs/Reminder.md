# Reminder


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**method** | [**ReminderMethod**](ReminderMethod.md) |  | 
**minutes** | **int** | Trigger time in minutes before the event start. | 

## Example

```python
from spatio.models.reminder import Reminder

# TODO update the JSON string below
json = "{}"
# create an instance of Reminder from a JSON string
reminder_instance = Reminder.from_json(json)
# print the JSON string representation of the object
print(Reminder.to_json())

# convert the object into a dict
reminder_dict = reminder_instance.to_dict()
# create an instance of Reminder from a dict
reminder_from_dict = Reminder.from_dict(reminder_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


