# SdkWhatsappWebMultiDevice\AppApi

Initial Connection to Whatsapp server

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appDevices()**](AppApi.md#appDevices) | **GET** /app/devices | Get list connected devices |
| [**appLogin()**](AppApi.md#appLogin) | **GET** /app/login | Login to whatsapp server |
| [**appLoginWithCode()**](AppApi.md#appLoginWithCode) | **GET** /app/login-with-code | Login with pairing code |
| [**appLogout()**](AppApi.md#appLogout) | **GET** /app/logout | Remove database and logout |
| [**appReconnect()**](AppApi.md#appReconnect) | **GET** /app/reconnect | Reconnecting to whatsapp server |
| [**appStatus()**](AppApi.md#appStatus) | **GET** /app/status | Get connection status |


## `appDevices()`

```php
appDevices(): \SdkWhatsappWebMultiDevice\Model\DeviceResponse
```

Get list connected devices

Returns all device IDs known to the server, including placeholders created via the device API. Devices are now persisted in the storage registry so IDs remain stable after application restarts.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->appDevices();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appDevices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DeviceResponse**](../Model/DeviceResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLogin()`

```php
appLogin($x_device_id): \SdkWhatsappWebMultiDevice\Model\LoginResponse
```

Login to whatsapp server

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->appLogin($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLogin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\LoginResponse**](../Model/LoginResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLoginWithCode()`

```php
appLoginWithCode($x_device_id, $phone): \SdkWhatsappWebMultiDevice\Model\LoginWithCodeResponse
```

Login with pairing code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$phone = 628912344551; // string | Your phone number

try {
    $result = $apiInstance->appLoginWithCode($x_device_id, $phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLoginWithCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **phone** | **string**| Your phone number | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\LoginWithCodeResponse**](../Model/LoginWithCodeResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLogout()`

```php
appLogout($x_device_id): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Remove database and logout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->appLogout($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLogout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appReconnect()`

```php
appReconnect($x_device_id): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Reconnecting to whatsapp server

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->appReconnect($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appReconnect: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appStatus()`

```php
appStatus($x_device_id): \SdkWhatsappWebMultiDevice\Model\AppStatus200Response
```

Get connection status

Check whether the WhatsApp client is connected and logged in

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->appStatus($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\AppStatus200Response**](../Model/AppStatus200Response.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
