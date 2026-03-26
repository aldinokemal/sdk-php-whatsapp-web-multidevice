# SdkWhatsappWebMultiDevice\ChatApi

Chat conversations and messaging

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**archiveChat()**](ChatApi.md#archiveChat) | **POST** /chat/{chat_jid}/archive | Archive or unarchive a chat |
| [**getChatMessages()**](ChatApi.md#getChatMessages) | **GET** /chat/{chat_jid}/messages | Get messages from a specific chat |
| [**labelChat()**](ChatApi.md#labelChat) | **POST** /chat/{chat_jid}/label | Label or unlabel a chat |
| [**listChats()**](ChatApi.md#listChats) | **GET** /chats | Get list of chats |
| [**pinChat()**](ChatApi.md#pinChat) | **POST** /chat/{chat_jid}/pin | Pin or unpin a chat |
| [**setDisappearingTimer()**](ChatApi.md#setDisappearingTimer) | **POST** /chat/{chat_jid}/disappearing | Set disappearing messages timer |


## `archiveChat()`

```php
archiveChat($chat_jid, $x_device_id, $archive_chat_request): \SdkWhatsappWebMultiDevice\Model\ArchiveChatResponse
```

Archive or unarchive a chat

Archive or unarchive a chat conversation. Archived chats are hidden from the main chat list.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chat_jid = 6289685028129@s.whatsapp.net; // string | Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group)
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$archive_chat_request = new \SdkWhatsappWebMultiDevice\Model\ArchiveChatRequest(); // \SdkWhatsappWebMultiDevice\Model\ArchiveChatRequest

try {
    $result = $apiInstance->archiveChat($chat_jid, $x_device_id, $archive_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->archiveChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **archive_chat_request** | [**\SdkWhatsappWebMultiDevice\Model\ArchiveChatRequest**](../Model/ArchiveChatRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ArchiveChatResponse**](../Model/ArchiveChatResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getChatMessages()`

```php
getChatMessages($chat_jid, $x_device_id, $limit, $offset, $start_time, $end_time, $media_only, $is_from_me, $search): \SdkWhatsappWebMultiDevice\Model\ChatMessagesResponse
```

Get messages from a specific chat

Retrieve messages from a specific chat conversation with filtering options

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chat_jid = 6289685028129@s.whatsapp.net; // string | Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group)
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$limit = 50; // int | Maximum number of messages to return
$offset = 0; // int | Number of messages to skip (for pagination)
$start_time = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Filter messages from this timestamp (ISO 8601 format)
$end_time = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Filter messages until this timestamp (ISO 8601 format)
$media_only = false; // bool | Only return messages with media content
$is_from_me = True; // bool | Filter messages by sender (true for messages sent by you, false for received messages). When both media_only=true and isFromMe=false are provided, media_only takes precedence and will return all media messages regardless of sender.
$search = 'search_example'; // string | Search messages by content text

try {
    $result = $apiInstance->getChatMessages($chat_jid, $x_device_id, $limit, $offset, $start_time, $end_time, $media_only, $is_from_me, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->getChatMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **limit** | **int**| Maximum number of messages to return | [optional] [default to 50] |
| **offset** | **int**| Number of messages to skip (for pagination) | [optional] [default to 0] |
| **start_time** | **\DateTime**| Filter messages from this timestamp (ISO 8601 format) | [optional] |
| **end_time** | **\DateTime**| Filter messages until this timestamp (ISO 8601 format) | [optional] |
| **media_only** | **bool**| Only return messages with media content | [optional] [default to false] |
| **is_from_me** | **bool**| Filter messages by sender (true for messages sent by you, false for received messages). When both media_only&#x3D;true and isFromMe&#x3D;false are provided, media_only takes precedence and will return all media messages regardless of sender. | [optional] |
| **search** | **string**| Search messages by content text | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ChatMessagesResponse**](../Model/ChatMessagesResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `labelChat()`

```php
labelChat($chat_jid, $x_device_id, $label_chat_request): \SdkWhatsappWebMultiDevice\Model\LabelChatResponse
```

Label or unlabel a chat

Apply or remove a label from a chat conversation

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chat_jid = 6289685028129@s.whatsapp.net; // string | Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group)
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$label_chat_request = new \SdkWhatsappWebMultiDevice\Model\LabelChatRequest(); // \SdkWhatsappWebMultiDevice\Model\LabelChatRequest

try {
    $result = $apiInstance->labelChat($chat_jid, $x_device_id, $label_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->labelChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **label_chat_request** | [**\SdkWhatsappWebMultiDevice\Model\LabelChatRequest**](../Model/LabelChatRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\LabelChatResponse**](../Model/LabelChatResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listChats()`

```php
listChats($x_device_id, $limit, $offset, $search, $has_media, $archived): \SdkWhatsappWebMultiDevice\Model\ChatListResponse
```

Get list of chats

Retrieve a list of chat conversations with their basic information

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$limit = 25; // int | Maximum number of chats to return
$offset = 0; // int | Number of chats to skip (for pagination)
$search = 'search_example'; // string | Search chats by name
$has_media = false; // bool | Filter chats that contain media messages
$archived = True; // bool | Filter by archived status. true = archived only, false = non-archived only. Omit to return all chats.

try {
    $result = $apiInstance->listChats($x_device_id, $limit, $offset, $search, $has_media, $archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->listChats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **limit** | **int**| Maximum number of chats to return | [optional] [default to 25] |
| **offset** | **int**| Number of chats to skip (for pagination) | [optional] [default to 0] |
| **search** | **string**| Search chats by name | [optional] |
| **has_media** | **bool**| Filter chats that contain media messages | [optional] [default to false] |
| **archived** | **bool**| Filter by archived status. true &#x3D; archived only, false &#x3D; non-archived only. Omit to return all chats. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ChatListResponse**](../Model/ChatListResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `pinChat()`

```php
pinChat($chat_jid, $x_device_id, $pin_chat_request): \SdkWhatsappWebMultiDevice\Model\PinChatResponse
```

Pin or unpin a chat

Pin or unpin a chat conversation to the top of the chat list

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chat_jid = 6289685028129@s.whatsapp.net; // string | Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group)
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$pin_chat_request = new \SdkWhatsappWebMultiDevice\Model\PinChatRequest(); // \SdkWhatsappWebMultiDevice\Model\PinChatRequest

try {
    $result = $apiInstance->pinChat($chat_jid, $x_device_id, $pin_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->pinChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **pin_chat_request** | [**\SdkWhatsappWebMultiDevice\Model\PinChatRequest**](../Model/PinChatRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\PinChatResponse**](../Model/PinChatResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setDisappearingTimer()`

```php
setDisappearingTimer($chat_jid, $x_device_id, $set_disappearing_timer_request): \SdkWhatsappWebMultiDevice\Model\SetDisappearingTimerResponse
```

Set disappearing messages timer

Set or disable disappearing messages for a chat. Valid timer values are 0 (off), 86400 (24h), 604800 (7d), 7776000 (90d).

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chat_jid = 6289685028129@s.whatsapp.net; // string | Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group)
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$set_disappearing_timer_request = new \SdkWhatsappWebMultiDevice\Model\SetDisappearingTimerRequest(); // \SdkWhatsappWebMultiDevice\Model\SetDisappearingTimerRequest

try {
    $result = $apiInstance->setDisappearingTimer($chat_jid, $x_device_id, $set_disappearing_timer_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->setDisappearingTimer: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **set_disappearing_timer_request** | [**\SdkWhatsappWebMultiDevice\Model\SetDisappearingTimerRequest**](../Model/SetDisappearingTimerRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SetDisappearingTimerResponse**](../Model/SetDisappearingTimerResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
