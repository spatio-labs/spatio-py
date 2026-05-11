# EnableShareRequest

Body for `POST /v1/notes/{id}/share`. With `setPassword: false`, only the public flag is flipped — any existing password is preserved. With `setPassword: true`, the supplied `password` is applied (an empty string clears it). 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**set_password** | **bool** |  | [optional] 
**password** | **str** |  | [optional] 

## Example

```python
from spatio.models.enable_share_request import EnableShareRequest

# TODO update the JSON string below
json = "{}"
# create an instance of EnableShareRequest from a JSON string
enable_share_request_instance = EnableShareRequest.from_json(json)
# print the JSON string representation of the object
print(EnableShareRequest.to_json())

# convert the object into a dict
enable_share_request_dict = enable_share_request_instance.to_dict()
# create an instance of EnableShareRequest from a dict
enable_share_request_from_dict = EnableShareRequest.from_dict(enable_share_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


