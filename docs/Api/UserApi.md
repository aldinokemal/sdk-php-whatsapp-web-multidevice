# OpenAPI\Client\UserApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**userAvatar()**](UserApi.md#userAvatar) | **GET** /user/avatar | User Avatar |
| [**userInfo()**](UserApi.md#userInfo) | **GET** /user/info | User Info |
| [**userMyGroups()**](UserApi.md#userMyGroups) | **GET** /user/my/groups | User My List Groups |
| [**userMyPrivacy()**](UserApi.md#userMyPrivacy) | **GET** /user/my/privacy | User My Privacy Setting |


## `userAvatar()`

```php
userAvatar($phone, $is_preview): \OpenAPI\Client\Model\UserAvatarResponse
```

User Avatar

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone = 6289685028129@s.whatsapp.net; // int
$is_preview = true; // bool

try {
    $result = $apiInstance->userAvatar($phone, $is_preview);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userAvatar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone** | **int**|  | [optional] |
| **is_preview** | **bool**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\UserAvatarResponse**](../Model/UserAvatarResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userInfo()`

```php
userInfo($phone): \OpenAPI\Client\Model\UserInfoResponse
```

User Info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$phone = 6289685028129@s.whatsapp.net; // int

try {
    $result = $apiInstance->userInfo($phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone** | **int**|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\UserInfoResponse**](../Model/UserInfoResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyGroups()`

```php
userMyGroups()
```

User My List Groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $apiInstance->userMyGroups();
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

void (empty response body)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyPrivacy()`

```php
userMyPrivacy(): \OpenAPI\Client\Model\UserPrivacyResponse
```

User My Privacy Setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);

try {
    $result = $apiInstance->userMyPrivacy();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyPrivacy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\OpenAPI\Client\Model\UserPrivacyResponse**](../Model/UserPrivacyResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
