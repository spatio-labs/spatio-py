# Task

A to-do / reminder / issue. Tasks belong to one connected account (`accountId` + `provider`). Native tasks store in Spatio's DB; external providers (Linear, GitHub Issues, Todoist, etc.) round-trip through Spatio. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** | Registered provider id (e.g. &#x60;native-tasks&#x60;, &#x60;linear&#x60;). | [optional] 
**account_id** | **str** |  | [optional] 
**owner_user_id** | **str** |  | [optional] 
**title** | **str** |  | 
**description** | **str** |  | [optional] 
**status** | **str** | Free-form status string. Canonical values across most providers: &#x60;todo&#x60;, &#x60;in_progress&#x60;, &#x60;in_review&#x60;, &#x60;backlog&#x60;, &#x60;done&#x60;. The platform falls back to &#x60;done&#x60; when &#x60;completed&#x60; is true and &#x60;status&#x60; is empty, else &#x60;todo&#x60;.  | [optional] 
**completed** | **bool** |  | 
**due_date** | **datetime** |  | [optional] 
**priority** | **str** | Priority bucket. Canonical values (mapped from a 0–4 integer): &#x60;none&#x60;, &#x60;low&#x60;, &#x60;medium&#x60;, &#x60;high&#x60;, &#x60;urgent&#x60;.  | 
**labels** | **List[str]** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**assignee_id** | **str** |  | [optional] 
**created_at** | **datetime** |  | 
**updated_at** | **datetime** |  | 
**completed_at** | **datetime** |  | [optional] 
**parent_task_id** | **str** | Parent task id when this is a subtask. | [optional] 
**metadata** | **Dict[str, object]** | Provider-specific extras. | [optional] 
**type** | **str** | Discriminator. Canonical values: &#x60;todo&#x60;, &#x60;reminder&#x60;, &#x60;issue&#x60;. Empty defaults to &#x60;todo&#x60;.  | [optional] 
**source_platform** | **str** | When this task was auto-generated from another artifact (e.g. a calendar event reminder), the platform id of that artifact.  | [optional] 
**source_id** | **str** | Source artifact id paired with &#x60;sourcePlatform&#x60;. | [optional] 

## Example

```python
from spatio.models.task import Task

# TODO update the JSON string below
json = "{}"
# create an instance of Task from a JSON string
task_instance = Task.from_json(json)
# print the JSON string representation of the object
print(Task.to_json())

# convert the object into a dict
task_dict = task_instance.to_dict()
# create an instance of Task from a dict
task_from_dict = Task.from_dict(task_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


