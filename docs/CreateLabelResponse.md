# CreateLabelResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**label** | [**Label**](Label.md) |  | 
**provider** | **str** |  | 

## Example

```python
from spatio.models.create_label_response import CreateLabelResponse

# TODO update the JSON string below
json = "{}"
# create an instance of CreateLabelResponse from a JSON string
create_label_response_instance = CreateLabelResponse.from_json(json)
# print the JSON string representation of the object
print(CreateLabelResponse.to_json())

# convert the object into a dict
create_label_response_dict = create_label_response_instance.to_dict()
# create an instance of CreateLabelResponse from a dict
create_label_response_from_dict = CreateLabelResponse.from_dict(create_label_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


