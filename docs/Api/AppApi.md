# OpenAPI\Client\AppApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**appDevices()**](AppApi.md#appDevices) | **GET** /app/devices | Get list connected devices |
| [**appLogin()**](AppApi.md#appLogin) | **GET** /app/login | Login to whatsapp server |
| [**appLoginWithCode()**](AppApi.md#appLoginWithCode) | **GET** /app/login-with-code | Login with pairing code |
| [**appLogout()**](AppApi.md#appLogout) | **GET** /app/logout | Remove database and logout |
| [**appReconnect()**](AppApi.md#appReconnect) | **GET** /app/reconnect | Reconnecting to whatsapp server |


## `appDevices()`

```php
appDevices(): \OpenAPI\Client\Model\DeviceResponse
```

Get list connected devices

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
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

[**\OpenAPI\Client\Model\DeviceResponse**](../Model/DeviceResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLogin()`

```php
appLogin(): \OpenAPI\Client\Model\LoginResponse
```

Login to whatsapp server

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->appLogin();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLogin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\LoginResponse**](../Model/LoginResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLoginWithCode()`

```php
appLoginWithCode($phone): \OpenAPI\Client\Model\LoginWithCodeResponse
```

Login with pairing code

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone = 628912344551; // string | Your phone number

try {
    $result = $apiInstance->appLoginWithCode($phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLoginWithCode: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone** | **string**| Your phone number | [optional] |

### Return type

[**\OpenAPI\Client\Model\LoginWithCodeResponse**](../Model/LoginWithCodeResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appLogout()`

```php
appLogout(): \OpenAPI\Client\Model\GenericResponse
```

Remove database and logout

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->appLogout();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appLogout: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `appReconnect()`

```php
appReconnect(): \OpenAPI\Client\Model\GenericResponse
```

Reconnecting to whatsapp server

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\AppApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->appReconnect();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling AppApi->appReconnect: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
