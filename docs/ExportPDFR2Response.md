# ExportPDFR2Response

Response shape when the export was uploaded to R2 (`?storage=r2`). The streaming case (`?storage=stream`, default) returns a binary `application/pdf` body and is not modeled as a JSON schema. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**storage** | **str** |  | 
**url** | **str** | 24-hour signed URL. | 
**expires_at** | **datetime** |  | 
**size** | **int** | PDF size in bytes. | 

## Example

```python
from spatio.models.export_pdfr2_response import ExportPDFR2Response

# TODO update the JSON string below
json = "{}"
# create an instance of ExportPDFR2Response from a JSON string
export_pdfr2_response_instance = ExportPDFR2Response.from_json(json)
# print the JSON string representation of the object
print(ExportPDFR2Response.to_json())

# convert the object into a dict
export_pdfr2_response_dict = export_pdfr2_response_instance.to_dict()
# create an instance of ExportPDFR2Response from a dict
export_pdfr2_response_from_dict = ExportPDFR2Response.from_dict(export_pdfr2_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


