# UpdatePATRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 

## Example

```python
from spatio.models.update_pat_request import UpdatePATRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdatePATRequest from a JSON string
update_pat_request_instance = UpdatePATRequest.from_json(json)
# print the JSON string representation of the object
print(UpdatePATRequest.to_json())

# convert the object into a dict
update_pat_request_dict = update_pat_request_instance.to_dict()
# create an instance of UpdatePATRequest from a dict
update_pat_request_from_dict = UpdatePATRequest.from_dict(update_pat_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


