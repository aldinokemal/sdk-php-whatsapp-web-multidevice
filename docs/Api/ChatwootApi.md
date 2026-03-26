# SdkWhatsappWebMultiDevice\ChatwootApi

Chatwoot integration for customer support

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**chatwootSyncHistory()**](ChatwootApi.md#chatwootSyncHistory) | **POST** /chatwoot/sync | Sync message history to Chatwoot |
| [**chatwootSyncStatus()**](ChatwootApi.md#chatwootSyncStatus) | **GET** /chatwoot/sync/status | Get Chatwoot sync progress |
| [**chatwootWebhook()**](ChatwootApi.md#chatwootWebhook) | **POST** /chatwoot/webhook | Chatwoot webhook endpoint |


## `chatwootSyncHistory()`

```php
chatwootSyncHistory($chatwoot_sync_history_request): \SdkWhatsappWebMultiDevice\Model\ChatwootSyncResponse
```

Sync message history to Chatwoot

Initiates a background sync of WhatsApp message history to Chatwoot. Messages from the configured number of days will be imported. This endpoint requires CHATWOOT_ENABLED=true in configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatwootApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$chatwoot_sync_history_request = new \SdkWhatsappWebMultiDevice\Model\ChatwootSyncHistoryRequest(); // \SdkWhatsappWebMultiDevice\Model\ChatwootSyncHistoryRequest

try {
    $result = $apiInstance->chatwootSyncHistory($chatwoot_sync_history_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatwootApi->chatwootSyncHistory: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **chatwoot_sync_history_request** | [**\SdkWhatsappWebMultiDevice\Model\ChatwootSyncHistoryRequest**](../Model/ChatwootSyncHistoryRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ChatwootSyncResponse**](../Model/ChatwootSyncResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatwootSyncStatus()`

```php
chatwootSyncStatus($device_id): \SdkWhatsappWebMultiDevice\Model\ChatwootSyncStatusResponse
```

Get Chatwoot sync progress

Returns the current sync progress for a device

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatwootApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID to check sync status for

try {
    $result = $apiInstance->chatwootSyncStatus($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ChatwootApi->chatwootSyncStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID to check sync status for | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ChatwootSyncStatusResponse**](../Model/ChatwootSyncStatusResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `chatwootWebhook()`

```php
chatwootWebhook($body)
```

Chatwoot webhook endpoint

Receives webhook events from Chatwoot and sends messages to WhatsApp. Configure this URL in your Chatwoot inbox webhook settings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\ChatwootApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = array('key' => new \stdClass); // object

try {
    $apiInstance->chatwootWebhook($body);
} catch (Exception $e) {
    echo 'Exception when calling ChatwootApi->chatwootWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | **object**|  | [optional] |

### Return type

void (empty response body)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
