# SdkWhatsappWebMultiDevice\ChatApi

Chat conversations and messaging

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getChatMessages()**](ChatApi.md#getChatMessages) | **GET** /chat/{chat_jid}/messages | Get messages from a specific chat |
| [**labelChat()**](ChatApi.md#labelChat) | **POST** /chat/{chat_jid}/label | Label or unlabel a chat |
| [**listChats()**](ChatApi.md#listChats) | **GET** /chats | Get list of chats |
| [**pinChat()**](ChatApi.md#pinChat) | **POST** /chat/{chat_jid}/pin | Pin or unpin a chat |


## `getChatMessages()`

```php
getChatMessages($chat_jid, $limit, $offset, $start_time, $end_time, $media_only, $is_from_me, $search): \SdkWhatsappWebMultiDevice\Model\ChatMessagesResponse
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
$limit = 50; // int | Maximum number of messages to return
$offset = 0; // int | Number of messages to skip (for pagination)
$start_time = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Filter messages from this timestamp (ISO 8601 format)
$end_time = new \DateTime('2013-10-20T19:20:30+01:00'); // \DateTime | Filter messages until this timestamp (ISO 8601 format)
$media_only = false; // bool | Only return messages with media content
$is_from_me = True; // bool | Filter messages by sender (true for messages sent by you, false for received messages). When both media_only=true and isFromMe=false are provided, media_only takes precedence and will return all media messages regardless of sender.
$search = 'search_example'; // string | Search messages by content text

try {
    $result = $apiInstance->getChatMessages($chat_jid, $limit, $offset, $start_time, $end_time, $media_only, $is_from_me, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->getChatMessages: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
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
labelChat($chat_jid, $label_chat_request): \SdkWhatsappWebMultiDevice\Model\LabelChatResponse
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
$label_chat_request = new \SdkWhatsappWebMultiDevice\Model\LabelChatRequest(); // \SdkWhatsappWebMultiDevice\Model\LabelChatRequest

try {
    $result = $apiInstance->labelChat($chat_jid, $label_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->labelChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
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
listChats($limit, $offset, $search, $has_media): \SdkWhatsappWebMultiDevice\Model\ChatListResponse
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
$limit = 25; // int | Maximum number of chats to return
$offset = 0; // int | Number of chats to skip (for pagination)
$search = 'search_example'; // string | Search chats by name
$has_media = false; // bool | Filter chats that contain media messages

try {
    $result = $apiInstance->listChats($limit, $offset, $search, $has_media);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->listChats: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **limit** | **int**| Maximum number of chats to return | [optional] [default to 25] |
| **offset** | **int**| Number of chats to skip (for pagination) | [optional] [default to 0] |
| **search** | **string**| Search chats by name | [optional] |
| **has_media** | **bool**| Filter chats that contain media messages | [optional] [default to false] |

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
pinChat($chat_jid, $pin_chat_request): \SdkWhatsappWebMultiDevice\Model\PinChatResponse
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
$pin_chat_request = new \SdkWhatsappWebMultiDevice\Model\PinChatRequest(); // \SdkWhatsappWebMultiDevice\Model\PinChatRequest

try {
    $result = $apiInstance->pinChat($chat_jid, $pin_chat_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatApi->pinChat: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chat_jid** | **string**| Chat JID (e.g., phone@s.whatsapp.net for individual or groupid@g.us for group) | |
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
