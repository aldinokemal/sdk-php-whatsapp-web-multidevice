# SdkWhatsappWebMultiDevice\UserApi

Getting information

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**userAvatar()**](UserApi.md#userAvatar) | **GET** /user/avatar | User Avatar |
| [**userBusinessProfile()**](UserApi.md#userBusinessProfile) | **GET** /user/business-profile | Get Business Profile Information |
| [**userChangeAvatar()**](UserApi.md#userChangeAvatar) | **POST** /user/avatar | User Change Avatar |
| [**userChangePushName()**](UserApi.md#userChangePushName) | **POST** /user/pushname | User Change Push Name |
| [**userCheck()**](UserApi.md#userCheck) | **GET** /user/check | Check if user is on WhatsApp |
| [**userInfo()**](UserApi.md#userInfo) | **GET** /user/info | User Info |
| [**userMyContacts()**](UserApi.md#userMyContacts) | **GET** /user/my/contacts | Get list of user contacts |
| [**userMyGroups()**](UserApi.md#userMyGroups) | **GET** /user/my/groups | User My List Groups |
| [**userMyNewsletter()**](UserApi.md#userMyNewsletter) | **GET** /user/my/newsletters | User My List Groups |
| [**userMyPrivacy()**](UserApi.md#userMyPrivacy) | **GET** /user/my/privacy | User My Privacy Setting |


## `userAvatar()`

```php
userAvatar($x_device_id, $phone, $is_preview, $is_community): \SdkWhatsappWebMultiDevice\Model\UserAvatarResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code
$is_preview = true; // bool | Whether to fetch a preview of the avatar
$is_community = false; // bool | Whether to fetch a community avatar

try {
    $result = $apiInstance->userAvatar($x_device_id, $phone, $is_preview, $is_community);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userAvatar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **phone** | **string**| Phone number with country code | [optional] |
| **is_preview** | **bool**| Whether to fetch a preview of the avatar | [optional] |
| **is_community** | **bool**| Whether to fetch a community avatar | [optional] |

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

## `userBusinessProfile()`

```php
userBusinessProfile($phone, $x_device_id): \SdkWhatsappWebMultiDevice\Model\BusinessProfileResponse
```

Get Business Profile Information

Retrieve detailed business profile information for a WhatsApp business account

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
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code of the business account
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->userBusinessProfile($phone, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userBusinessProfile: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **phone** | **string**| Phone number with country code of the business account | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\BusinessProfileResponse**](../Model/BusinessProfileResponse.md)

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
userChangeAvatar($x_device_id, $avatar): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$avatar = '/path/to/file.txt'; // \SplFileObject | Avatar to send

try {
    $result = $apiInstance->userChangeAvatar($x_device_id, $avatar);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userChangeAvatar: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
userChangePushName($x_device_id, $user_change_push_name_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$user_change_push_name_request = new \SdkWhatsappWebMultiDevice\Model\UserChangePushNameRequest(); // \SdkWhatsappWebMultiDevice\Model\UserChangePushNameRequest

try {
    $result = $apiInstance->userChangePushName($x_device_id, $user_change_push_name_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userChangePushName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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

## `userCheck()`

```php
userCheck($x_device_id, $phone): \SdkWhatsappWebMultiDevice\Model\UserCheckResponse
```

Check if user is on WhatsApp

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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$phone = 628912344551; // string | Phone number with country code

try {
    $result = $apiInstance->userCheck($x_device_id, $phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userCheck: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **phone** | **string**| Phone number with country code | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\UserCheckResponse**](../Model/UserCheckResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `userInfo()`

```php
userInfo($x_device_id, $phone): \SdkWhatsappWebMultiDevice\Model\UserInfoResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$phone = 6289685028129@s.whatsapp.net; // string | Phone number with country code

try {
    $result = $apiInstance->userInfo($x_device_id, $phone);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
userMyContacts($x_device_id): \SdkWhatsappWebMultiDevice\Model\MyListContactsResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->userMyContacts($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyContacts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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
userMyGroups($x_device_id): \SdkWhatsappWebMultiDevice\Model\UserGroupResponse
```

User My List Groups

Get all groups that the authenticated user has joined.  ⚠️ **Known Limitation**: This endpoint returns a maximum of 500 groups due to a WhatsApp protocol limitation. The underlying whatsmeow library's `GetJoinedGroups()` function sends a single query to WhatsApp servers, which enforces this limit. This is not a bug in this API - it's a constraint imposed by WhatsApp's multi-device protocol. Users with more than 500 groups will only receive the first 500 groups.  For more details, see: https://github.com/tulir/whatsmeow/blob/main/group.go

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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->userMyGroups($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyGroups: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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
userMyNewsletter($x_device_id): \SdkWhatsappWebMultiDevice\Model\NewsletterResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->userMyNewsletter($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyNewsletter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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
userMyPrivacy($x_device_id): \SdkWhatsappWebMultiDevice\Model\UserPrivacyResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->userMyPrivacy($x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling UserApi->userMyPrivacy: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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
