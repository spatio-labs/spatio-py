# ChannelMembershipRequest

Body for join/leave operations.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**account_id** | **str** |  | [optional] 

## Example

```python
from spatio.models.channel_membership_request import ChannelMembershipRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ChannelMembershipRequest from a JSON string
channel_membership_request_instance = ChannelMembershipRequest.from_json(json)
# print the JSON string representation of the object
print(ChannelMembershipRequest.to_json())

# convert the object into a dict
channel_membership_request_dict = channel_membership_request_instance.to_dict()
# create an instance of ChannelMembershipRequest from a dict
channel_membership_request_from_dict = ChannelMembershipRequest.from_dict(channel_membership_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


