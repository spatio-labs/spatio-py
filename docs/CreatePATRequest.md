# CreatePATRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**scopes** | **List[str]** |  | [optional] 
**workspace_id** | **str** |  | [optional] 
**expires_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.create_pat_request import CreatePATRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreatePATRequest from a JSON string
create_pat_request_instance = CreatePATRequest.from_json(json)
# print the JSON string representation of the object
print(CreatePATRequest.to_json())

# convert the object into a dict
create_pat_request_dict = create_pat_request_instance.to_dict()
# create an instance of CreatePATRequest from a dict
create_pat_request_from_dict = CreatePATRequest.from_dict(create_pat_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


