# ExtractTextResult

Extracted text + structural metadata from a PDF (or other extraction-supported file type). `pages` is provider-shaped — treat as an opaque per-page object array. Endpoint returns `422` with `code: extraction_unsupported` when the underlying file isn't extractable. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**text** | **str** |  | 
**page_count** | **int** |  | 
**pages** | **List[Dict[str, object]]** |  | [optional] 
**truncated** | **bool** | &#x60;true&#x60; when &#x60;maxChars&#x60; was hit before the end. | [optional] 

## Example

```python
from spatio.models.extract_text_result import ExtractTextResult

# TODO update the JSON string below
json = "{}"
# create an instance of ExtractTextResult from a JSON string
extract_text_result_instance = ExtractTextResult.from_json(json)
# print the JSON string representation of the object
print(ExtractTextResult.to_json())

# convert the object into a dict
extract_text_result_dict = extract_text_result_instance.to_dict()
# create an instance of ExtractTextResult from a dict
extract_text_result_from_dict = ExtractTextResult.from_dict(extract_text_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


