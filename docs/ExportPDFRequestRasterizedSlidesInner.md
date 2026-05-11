# ExportPDFRequestRasterizedSlidesInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**slide_id** | **str** |  | 
**png** | **str** | Base64-encoded PNG. | 

## Example

```python
from spatio.models.export_pdf_request_rasterized_slides_inner import ExportPDFRequestRasterizedSlidesInner

# TODO update the JSON string below
json = "{}"
# create an instance of ExportPDFRequestRasterizedSlidesInner from a JSON string
export_pdf_request_rasterized_slides_inner_instance = ExportPDFRequestRasterizedSlidesInner.from_json(json)
# print the JSON string representation of the object
print(ExportPDFRequestRasterizedSlidesInner.to_json())

# convert the object into a dict
export_pdf_request_rasterized_slides_inner_dict = export_pdf_request_rasterized_slides_inner_instance.to_dict()
# create an instance of ExportPDFRequestRasterizedSlidesInner from a dict
export_pdf_request_rasterized_slides_inner_from_dict = ExportPDFRequestRasterizedSlidesInner.from_dict(export_pdf_request_rasterized_slides_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


