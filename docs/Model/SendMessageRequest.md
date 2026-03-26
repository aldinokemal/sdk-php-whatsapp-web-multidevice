# SendMessageRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phone** | **string** | Phone number with country code | [optional]
**message** | **string** | Message to send | [optional]
**reply_message_id** | **string** | Message ID that you want reply | [optional]
**is_forwarded** | **bool** | Whether this is a forwarded message | [optional]
**duration** | **int** | Disappearing message duration in seconds (optional) | [optional]
**mentions** | **string[]** | List of phone numbers to mention (ghost mentions - no @ required in message text). Use special keyword \&quot;@everyone\&quot; to mention all group participants. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
