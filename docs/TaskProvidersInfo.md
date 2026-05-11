# TaskProvidersInfo

Metadata about which task providers are connected and what the Tasks platform itself reports for its name + description. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**providers** | **List[str]** | Registered provider ids (e.g. &#x60;native-tasks&#x60;, &#x60;linear&#x60;). | 
**platform** | [**TaskProvidersInfoPlatform**](TaskProvidersInfoPlatform.md) |  | 

## Example

```python
from spatio.models.task_providers_info import TaskProvidersInfo

# TODO update the JSON string below
json = "{}"
# create an instance of TaskProvidersInfo from a JSON string
task_providers_info_instance = TaskProvidersInfo.from_json(json)
# print the JSON string representation of the object
print(TaskProvidersInfo.to_json())

# convert the object into a dict
task_providers_info_dict = task_providers_info_instance.to_dict()
# create an instance of TaskProvidersInfo from a dict
task_providers_info_from_dict = TaskProvidersInfo.from_dict(task_providers_info_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


