# BlockContent

Type-specific payload for a block. Fields populated depend on `Block.type`. All fields are optional at the schema level; the runtime enforces the per-type contract.  Note: this object uses snake_case keys to match the JSON the Go `providers.BlockContent` struct emits and accepts. Other parts of the SpatioAPI use camelCase; blocks are the exception because the block model is shared with external Notion-like providers whose canonical wire format is snake_case. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**rich_text** | [**List[RichTextObject]**](RichTextObject.md) |  | [optional] 
**language** | **str** | Programming language for &#x60;code&#x60; blocks. | [optional] 
**checked** | **bool** | Toggle state for &#x60;to_do&#x60; blocks. | [optional] 
**icon** | **str** | Emoji or short string for &#x60;callout&#x60; blocks. | [optional] 
**color** | **str** | Theme color for &#x60;callout&#x60; blocks. | [optional] 
**url** | **str** | Source URL for &#x60;image&#x60;, &#x60;video&#x60;, &#x60;file&#x60; blocks. | [optional] 
**caption** | **str** | Visible caption for media blocks. | [optional] 
**alt_text** | **str** | Screen-reader description for media blocks. Distinct from &#x60;caption&#x60; (visible to readers) — required for accessible notes when the image conveys meaning.  | [optional] 
**embed_url** | **str** | Source URL for &#x60;embed&#x60; blocks. | [optional] 
**cells** | **List[List[RichTextObject]]** | 2D rich-text grid for &#x60;table&#x60; and &#x60;table_row&#x60; blocks. | [optional] 
**expression** | **str** | TeX/MathJax expression for &#x60;equation&#x60; blocks. | [optional] 

## Example

```python
from spatio.models.block_content import BlockContent

# TODO update the JSON string below
json = "{}"
# create an instance of BlockContent from a JSON string
block_content_instance = BlockContent.from_json(json)
# print the JSON string representation of the object
print(BlockContent.to_json())

# convert the object into a dict
block_content_dict = block_content_instance.to_dict()
# create an instance of BlockContent from a dict
block_content_from_dict = BlockContent.from_dict(block_content_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


