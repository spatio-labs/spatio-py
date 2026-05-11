# Channel

A chat conversation. The same struct backs both group channels (`type: channel | private`) and direct-message threads (`type: im | mpim`); the `Channels` and `DirectMessages` HTTP surfaces filter on `type` to give each its dedicated URL space. 

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**provider** | **str** | Registered provider id (e.g. &#x60;slack&#x60;, &#x60;native-chat&#x60;).  | [optional] 
**account_id** | **str** |  | [optional] 
**name** | **str** |  | 
**type** | **str** | Provider-specific. Common canonicals: &#x60;channel&#x60; and &#x60;private&#x60; (group channels), &#x60;im&#x60; (1:1 DM), &#x60;mpim&#x60; (group DM).  | 
**description** | **str** |  | [optional] 
**topic** | **str** |  | [optional] 
**is_member** | **bool** |  | 
**is_archived** | **bool** |  | 
**member_count** | **int** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from spatio.models.channel import Channel

# TODO update the JSON string below
json = "{}"
# create an instance of Channel from a JSON string
channel_instance = Channel.from_json(json)
# print the JSON string representation of the object
print(Channel.to_json())

# convert the object into a dict
channel_dict = channel_instance.to_dict()
# create an instance of Channel from a dict
channel_from_dict = Channel.from_dict(channel_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


