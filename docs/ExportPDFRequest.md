# ExportPDFRequest

Optional body for `POST /v1/slides/{id}/export/pdf`. Renderer posts pre-rasterized PNGs for slides that contain Fabric.js elements (the sidecar can't run Fabric server-side); slides without an entry are rendered from their `layout` + theme. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rasterized_slides** | [**List[ExportPDFRequestRasterizedSlidesInner]**](ExportPDFRequestRasterizedSlidesInner.md) |  | [optional] 
**theme** | **Dict[str, object]** | Optional palette override. Schemaless — the export sidecar accepts a free-form palette object. Treat as opaque.  | [optional] 

## Example

```python
from spatio.models.export_pdf_request import ExportPDFRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ExportPDFRequest from a JSON string
export_pdf_request_instance = ExportPDFRequest.from_json(json)
# print the JSON string representation of the object
print(ExportPDFRequest.to_json())

# convert the object into a dict
export_pdf_request_dict = export_pdf_request_instance.to_dict()
# create an instance of ExportPDFRequest from a dict
export_pdf_request_from_dict = ExportPDFRequest.from_dict(export_pdf_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


