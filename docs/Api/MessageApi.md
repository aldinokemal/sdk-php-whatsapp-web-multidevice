# SdkWhatsappWebMultiDevice\MessageApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteMessage()**](MessageApi.md#deleteMessage) | **POST** /message/{message_id}/delete | Delete Message |
| [**reactMessage()**](MessageApi.md#reactMessage) | **POST** /message/{message_id}/reaction | Send reaction to message |
| [**revokeMessage()**](MessageApi.md#revokeMessage) | **POST** /message/{message_id}/revoke | Revoke Message |
| [**updateMessage()**](MessageApi.md#updateMessage) | **POST** /message/{message_id}/update | Edit message by message ID before 15 minutes |


## `deleteMessage()`

```php
deleteMessage($message_id, $revoke_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Delete Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 'message_id_example'; // string | Message ID
$revoke_message_request = new \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest

try {
    $result = $apiInstance->deleteMessage($message_id, $revoke_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->deleteMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **revoke_message_request** | [**\SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest**](../Model/RevokeMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactMessage()`

```php
reactMessage($message_id, $react_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Send reaction to message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 'message_id_example'; // string | Message ID
$react_message_request = new \SdkWhatsappWebMultiDevice\Model\ReactMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\ReactMessageRequest

try {
    $result = $apiInstance->reactMessage($message_id, $react_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->reactMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **react_message_request** | [**\SdkWhatsappWebMultiDevice\Model\ReactMessageRequest**](../Model/ReactMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeMessage()`

```php
revokeMessage($message_id, $revoke_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Revoke Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 'message_id_example'; // string | Message ID
$revoke_message_request = new \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest

try {
    $result = $apiInstance->revokeMessage($message_id, $revoke_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->revokeMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **revoke_message_request** | [**\SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest**](../Model/RevokeMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateMessage()`

```php
updateMessage($message_id, $update_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Edit message by message ID before 15 minutes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$message_id = 'message_id_example'; // string | Message ID
$update_message_request = new \SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest

try {
    $result = $apiInstance->updateMessage($message_id, $update_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->updateMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **update_message_request** | [**\SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest**](../Model/UpdateMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
