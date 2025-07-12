# # ChatMessage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Message ID | [optional]
**chat_jid** | **string** | Chat JID this message belongs to | [optional]
**sender_jid** | **string** | Sender JID | [optional]
**content** | **string** | Message text content | [optional]
**timestamp** | **\DateTime** | Message timestamp | [optional]
**is_from_me** | **bool** | Whether this message was sent by the current user | [optional]
**media_type** | **string** | Type of media (image, video, audio, document, etc.) | [optional]
**filename** | **string** | Original filename for media messages | [optional]
**url** | **string** | Media file URL | [optional]
**file_length** | **int** | File size in bytes for media messages | [optional]
**created_at** | **\DateTime** | Record creation timestamp | [optional]
**updated_at** | **\DateTime** | Record last update timestamp | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
