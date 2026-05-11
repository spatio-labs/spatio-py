# ListEventsData

Shape of `data` when returned by `listEvents`. Wrapped inside a CalendarOperationResult — clients should access this as `result.data` after checking `result.success`. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**events** | [**List[SpatioEvent]**](SpatioEvent.md) | &#x60;null&#x60; when there are no results (Go nil-slice serialization).  | [optional] 
**next_page_token** | **str** |  | [optional] 
**total_results** | **int** |  | [optional] 
**updated_at** | **datetime** |  | 

## Example

```python
from spatio.models.list_events_data import ListEventsData

# TODO update the JSON string below
json = "{}"
# create an instance of ListEventsData from a JSON string
list_events_data_instance = ListEventsData.from_json(json)
# print the JSON string representation of the object
print(ListEventsData.to_json())

# convert the object into a dict
list_events_data_dict = list_events_data_instance.to_dict()
# create an instance of ListEventsData from a dict
list_events_data_from_dict = ListEventsData.from_dict(list_events_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


