# SdkWhatsappWebMultiDevice\DeviceApi

Device management for multi-device support

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addDevice()**](DeviceApi.md#addDevice) | **POST** /devices | Add a new device |
| [**getDevice()**](DeviceApi.md#getDevice) | **GET** /devices/{device_id} | Get device info |
| [**getDeviceStatus()**](DeviceApi.md#getDeviceStatus) | **GET** /devices/{device_id}/status | Get device connection status |
| [**listDevices()**](DeviceApi.md#listDevices) | **GET** /devices | List all devices |
| [**loginDevice()**](DeviceApi.md#loginDevice) | **GET** /devices/{device_id}/login | Login device with QR code |
| [**loginDeviceWithCode()**](DeviceApi.md#loginDeviceWithCode) | **POST** /devices/{device_id}/login/code | Login device with pairing code |
| [**logoutDevice()**](DeviceApi.md#logoutDevice) | **POST** /devices/{device_id}/logout | Logout device |
| [**reconnectDevice()**](DeviceApi.md#reconnectDevice) | **POST** /devices/{device_id}/reconnect | Reconnect device |
| [**removeDevice()**](DeviceApi.md#removeDevice) | **DELETE** /devices/{device_id} | Remove a device |


## `addDevice()`

```php
addDevice($add_device_request): \SdkWhatsappWebMultiDevice\Model\DeviceAddResponse
```

Add a new device

Create a new device slot for multi-device management

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$add_device_request = new \SdkWhatsappWebMultiDevice\Model\AddDeviceRequest(); // \SdkWhatsappWebMultiDevice\Model\AddDeviceRequest

try {
    $result = $apiInstance->addDevice($add_device_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->addDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **add_device_request** | [**\SdkWhatsappWebMultiDevice\Model\AddDeviceRequest**](../Model/AddDeviceRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DeviceAddResponse**](../Model/DeviceAddResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDevice()`

```php
getDevice($device_id): \SdkWhatsappWebMultiDevice\Model\DeviceInfoResponse
```

Get device info

Get detailed information about a specific device

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->getDevice($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->getDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DeviceInfoResponse**](../Model/DeviceInfoResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getDeviceStatus()`

```php
getDeviceStatus($device_id): \SdkWhatsappWebMultiDevice\Model\DeviceStatusResponse
```

Get device connection status

Get the current connection status of a specific device

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->getDeviceStatus($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->getDeviceStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DeviceStatusResponse**](../Model/DeviceStatusResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listDevices()`

```php
listDevices(): \SdkWhatsappWebMultiDevice\Model\DeviceListResponse
```

List all devices

Returns all registered devices with their connection status

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listDevices();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->listDevices: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\SdkWhatsappWebMultiDevice\Model\DeviceListResponse**](../Model/DeviceListResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `loginDevice()`

```php
loginDevice($device_id): \SdkWhatsappWebMultiDevice\Model\LoginResponse
```

Login device with QR code

Initiate QR code login for a specific device

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->loginDevice($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->loginDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

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

## `loginDeviceWithCode()`

```php
loginDeviceWithCode($device_id, $phone): \SdkWhatsappWebMultiDevice\Model\LoginWithCodeResponse
```

Login device with pairing code

Initiate pairing code login for a specific device

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID
$phone = 628912344551; // string | Phone number to pair with

try {
    $result = $apiInstance->loginDeviceWithCode($device_id, $phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->loginDeviceWithCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |
| **phone** | **string**| Phone number to pair with | |

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

## `logoutDevice()`

```php
logoutDevice($device_id): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Logout device

Logout a specific device from WhatsApp and remove its session

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->logoutDevice($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->logoutDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

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

## `reconnectDevice()`

```php
reconnectDevice($device_id): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Reconnect device

Reconnect a specific device to WhatsApp

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->reconnectDevice($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->reconnectDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

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

## `removeDevice()`

```php
removeDevice($device_id): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Remove a device

Remove a device from the server (does not logout from WhatsApp)

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\DeviceApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$device_id = 'device_id_example'; // string | Device ID

try {
    $result = $apiInstance->removeDevice($device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DeviceApi->removeDevice: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **device_id** | **string**| Device ID | |

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
