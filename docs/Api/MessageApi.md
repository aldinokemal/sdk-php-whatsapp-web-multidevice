# SdkWhatsappWebMultiDevice\MessageApi

Message manipulation (revoke/react/update).

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteMessage()**](MessageApi.md#deleteMessage) | **POST** /message/{message_id}/delete | Delete Message |
| [**downloadMessageMedia()**](MessageApi.md#downloadMessageMedia) | **GET** /message/{message_id}/download | Download media from message |
| [**reactMessage()**](MessageApi.md#reactMessage) | **POST** /message/{message_id}/reaction | Send reaction to message |
| [**readMessage()**](MessageApi.md#readMessage) | **POST** /message/{message_id}/read | Mark as read message |
| [**revokeMessage()**](MessageApi.md#revokeMessage) | **POST** /message/{message_id}/revoke | Revoke Message |
| [**starMessage()**](MessageApi.md#starMessage) | **POST** /message/{message_id}/star | Star message |
| [**unstarMessage()**](MessageApi.md#unstarMessage) | **POST** /message/{message_id}/unstar | Unstar message |
| [**updateMessage()**](MessageApi.md#updateMessage) | **POST** /message/{message_id}/update | Edit message by message ID before 15 minutes |


## `deleteMessage()`

```php
deleteMessage($message_id, $x_device_id, $revoke_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Delete Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$revoke_message_request = new \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest

try {
    $result = $apiInstance->deleteMessage($message_id, $x_device_id, $revoke_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->deleteMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **revoke_message_request** | [**\SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest**](../Model/RevokeMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `downloadMessageMedia()`

```php
downloadMessageMedia($message_id, $phone, $x_device_id): \SdkWhatsappWebMultiDevice\Model\DownloadMessageMedia200Response
```

Download media from message

Download media content (image, video, audio, document) from a message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 3EB0123456789ABCDEF; // string | Message ID
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->downloadMessageMedia($message_id, $phone, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->downloadMessageMedia: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **phone** | **string**| Phone number with country code | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DownloadMessageMedia200Response**](../Model/DownloadMessageMedia200Response.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `reactMessage()`

```php
reactMessage($message_id, $x_device_id, $react_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Send reaction to message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$react_message_request = new \SdkWhatsappWebMultiDevice\Model\ReactMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\ReactMessageRequest

try {
    $result = $apiInstance->reactMessage($message_id, $x_device_id, $react_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->reactMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **react_message_request** | [**\SdkWhatsappWebMultiDevice\Model\ReactMessageRequest**](../Model/ReactMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `readMessage()`

```php
readMessage($message_id, $x_device_id, $read_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Mark as read message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$read_message_request = new \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest

try {
    $result = $apiInstance->readMessage($message_id, $x_device_id, $read_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->readMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **read_message_request** | [**\SdkWhatsappWebMultiDevice\Model\ReadMessageRequest**](../Model/ReadMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeMessage()`

```php
revokeMessage($message_id, $x_device_id, $revoke_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Revoke Message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$revoke_message_request = new \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest

try {
    $result = $apiInstance->revokeMessage($message_id, $x_device_id, $revoke_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->revokeMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **revoke_message_request** | [**\SdkWhatsappWebMultiDevice\Model\RevokeMessageRequest**](../Model/RevokeMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `starMessage()`

```php
starMessage($message_id, $x_device_id, $read_message_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Star message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$read_message_request = new \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest

try {
    $result = $apiInstance->starMessage($message_id, $x_device_id, $read_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->starMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **read_message_request** | [**\SdkWhatsappWebMultiDevice\Model\ReadMessageRequest**](../Model/ReadMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unstarMessage()`

```php
unstarMessage($message_id, $x_device_id, $read_message_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Unstar message

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$read_message_request = new \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\ReadMessageRequest

try {
    $result = $apiInstance->unstarMessage($message_id, $x_device_id, $read_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->unstarMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **read_message_request** | [**\SdkWhatsappWebMultiDevice\Model\ReadMessageRequest**](../Model/ReadMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateMessage()`

```php
updateMessage($message_id, $x_device_id, $update_message_request): \SdkWhatsappWebMultiDevice\Model\SendResponse
```

Edit message by message ID before 15 minutes

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\MessageApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$message_id = 'message_id_example'; // string | Message ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$update_message_request = new \SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest(); // \SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest

try {
    $result = $apiInstance->updateMessage($message_id, $x_device_id, $update_message_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling MessageApi->updateMessage: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **message_id** | **string**| Message ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **update_message_request** | [**\SdkWhatsappWebMultiDevice\Model\UpdateMessageRequest**](../Model/UpdateMessageRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SendResponse**](../Model/SendResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
