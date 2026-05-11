# DMSetDraftRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.dm_set_draft_request import DMSetDraftRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DMSetDraftRequest from a JSON string
dm_set_draft_request_instance = DMSetDraftRequest.from_json(json)
# print the JSON string representation of the object
print(DMSetDraftRequest.to_json())

# convert the object into a dict
dm_set_draft_request_dict = dm_set_draft_request_instance.to_dict()
# create an instance of DMSetDraftRequest from a dict
dm_set_draft_request_from_dict = DMSetDraftRequest.from_dict(dm_set_draft_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


