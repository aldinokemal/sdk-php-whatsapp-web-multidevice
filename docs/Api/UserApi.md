# SdkWhatsappWebMultiDevice\UserApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**userAvatar()**](UserApi.md#userAvatar) | **GET** /user/avatar | User Avatar |
| [**userChangeAvatar()**](UserApi.md#userChangeAvatar) | **POST** /user/avatar | User Change Avatar |
| [**userChangePushName()**](UserApi.md#userChangePushName) | **POST** /user/pushname | User Change Push Name |
| [**userInfo()**](UserApi.md#userInfo) | **GET** /user/info | User Info |
| [**userMyContacts()**](UserApi.md#userMyContacts) | **GET** /user/my/contacts | Get list of user contacts |
| [**userMyGroups()**](UserApi.md#userMyGroups) | **GET** /user/my/groups | User My List Groups |
| [**userMyNewsletter()**](UserApi.md#userMyNewsletter) | **GET** /user/my/newsletters | User My List Groups |
| [**userMyPrivacy()**](UserApi.md#userMyPrivacy) | **GET** /user/my/privacy | User My Privacy Setting |


## `userAvatar()`

```php
userAvatar($phone, $is_preview): \SdkWhatsappWebMultiDevice\Model\UserAvatarResponse
```

User Avatar

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code
$is_preview = true; // bool | Whether to fetch a preview of the avatar

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
| **phone** | **string**| Phone number with country code | [optional] |
| **is_preview** | **bool**| Whether to fetch a preview of the avatar | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\UserAvatarResponse**](../Model/UserAvatarResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userChangeAvatar()`

```php
userChangeAvatar($avatar): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

User Change Avatar

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$avatar = '/path/to/file.txt'; // \SplFileObject | Avatar to send

try {
    $result = $apiInstance->userChangeAvatar($avatar);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userChangeAvatar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **avatar** | **\SplFileObject****\SplFileObject**| Avatar to send | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userChangePushName()`

```php
userChangePushName($user_change_push_name_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

User Change Push Name

Update the display name (push name) shown to others in WhatsApp

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$user_change_push_name_request = new \SdkWhatsappWebMultiDevice\Model\UserChangePushNameRequest(); // \SdkWhatsappWebMultiDevice\Model\UserChangePushNameRequest

try {
    $result = $apiInstance->userChangePushName($user_change_push_name_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userChangePushName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **user_change_push_name_request** | [**\SdkWhatsappWebMultiDevice\Model\UserChangePushNameRequest**](../Model/UserChangePushNameRequest.md)|  | [optional] |

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

## `userInfo()`

```php
userInfo($phone): \SdkWhatsappWebMultiDevice\Model\UserInfoResponse
```

User Info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code

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
| **phone** | **string**| Phone number with country code | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\UserInfoResponse**](../Model/UserInfoResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyContacts()`

```php
userMyContacts(): \SdkWhatsappWebMultiDevice\Model\MyListContactsResponse
```

Get list of user contacts

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->userMyContacts();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\SdkWhatsappWebMultiDevice\Model\MyListContactsResponse**](../Model/MyListContactsResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyGroups()`

```php
userMyGroups(): \SdkWhatsappWebMultiDevice\Model\UserGroupResponse
```

User My List Groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->userMyGroups();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\SdkWhatsappWebMultiDevice\Model\UserGroupResponse**](../Model/UserGroupResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyNewsletter()`

```php
userMyNewsletter(): \SdkWhatsappWebMultiDevice\Model\NewsletterResponse
```

User My List Groups

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->userMyNewsletter();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyNewsletter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\SdkWhatsappWebMultiDevice\Model\NewsletterResponse**](../Model/NewsletterResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userMyPrivacy()`

```php
userMyPrivacy(): \SdkWhatsappWebMultiDevice\Model\UserPrivacyResponse
```

User My Privacy Setting

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\UserApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
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

[**\SdkWhatsappWebMultiDevice\Model\UserPrivacyResponse**](../Model/UserPrivacyResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
