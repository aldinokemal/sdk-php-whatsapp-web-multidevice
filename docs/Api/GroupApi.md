# OpenAPI\Client\GroupApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addParticipantToGroup()**](GroupApi.md#addParticipantToGroup) | **POST** /group/participants | Adding more participants to group |
| [**createGroup()**](GroupApi.md#createGroup) | **POST** /group | Create group and add participant |
| [**demoteParticipantToMember()**](GroupApi.md#demoteParticipantToMember) | **POST** /group/participants/demote | Demote participants to member |
| [**joinGroupWithLink()**](GroupApi.md#joinGroupWithLink) | **POST** /group/join-with-link | Join group with link |
| [**leaveGroup()**](GroupApi.md#leaveGroup) | **POST** /group/leave | Leave group |
| [**promoteParticipantToAdmin()**](GroupApi.md#promoteParticipantToAdmin) | **POST** /group/participants/promote | Promote participants to admin |
| [**removeParticipantFromGroup()**](GroupApi.md#removeParticipantFromGroup) | **POST** /group/participants/remove | Remove participants from group |


## `addParticipantToGroup()`

```php
addParticipantToGroup($manage_participant_request): \OpenAPI\Client\Model\ManageParticipantResponse
```

Adding more participants to group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$manage_participant_request = new \OpenAPI\Client\Model\ManageParticipantRequest(); // \OpenAPI\Client\Model\ManageParticipantRequest

try {
    $result = $apiInstance->addParticipantToGroup($manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->addParticipantToGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **manage_participant_request** | [**\OpenAPI\Client\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createGroup()`

```php
createGroup($create_group_request): \OpenAPI\Client\Model\CreateGroupResponse
```

Create group and add participant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$create_group_request = new \OpenAPI\Client\Model\CreateGroupRequest(); // \OpenAPI\Client\Model\CreateGroupRequest

try {
    $result = $apiInstance->createGroup($create_group_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->createGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **create_group_request** | [**\OpenAPI\Client\Model\CreateGroupRequest**](../Model/CreateGroupRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\CreateGroupResponse**](../Model/CreateGroupResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `demoteParticipantToMember()`

```php
demoteParticipantToMember($manage_participant_request): \OpenAPI\Client\Model\ManageParticipantResponse
```

Demote participants to member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$manage_participant_request = new \OpenAPI\Client\Model\ManageParticipantRequest(); // \OpenAPI\Client\Model\ManageParticipantRequest

try {
    $result = $apiInstance->demoteParticipantToMember($manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->demoteParticipantToMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **manage_participant_request** | [**\OpenAPI\Client\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `joinGroupWithLink()`

```php
joinGroupWithLink($join_group_with_link_request): \OpenAPI\Client\Model\GenericResponse
```

Join group with link

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$join_group_with_link_request = new \OpenAPI\Client\Model\JoinGroupWithLinkRequest(); // \OpenAPI\Client\Model\JoinGroupWithLinkRequest

try {
    $result = $apiInstance->joinGroupWithLink($join_group_with_link_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->joinGroupWithLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **join_group_with_link_request** | [**\OpenAPI\Client\Model\JoinGroupWithLinkRequest**](../Model/JoinGroupWithLinkRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `leaveGroup()`

```php
leaveGroup($leave_group_request): \OpenAPI\Client\Model\GenericResponse
```

Leave group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$leave_group_request = new \OpenAPI\Client\Model\LeaveGroupRequest(); // \OpenAPI\Client\Model\LeaveGroupRequest

try {
    $result = $apiInstance->leaveGroup($leave_group_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->leaveGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **leave_group_request** | [**\OpenAPI\Client\Model\LeaveGroupRequest**](../Model/LeaveGroupRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\GenericResponse**](../Model/GenericResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `promoteParticipantToAdmin()`

```php
promoteParticipantToAdmin($manage_participant_request): \OpenAPI\Client\Model\ManageParticipantResponse
```

Promote participants to admin

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$manage_participant_request = new \OpenAPI\Client\Model\ManageParticipantRequest(); // \OpenAPI\Client\Model\ManageParticipantRequest

try {
    $result = $apiInstance->promoteParticipantToAdmin($manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->promoteParticipantToAdmin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **manage_participant_request** | [**\OpenAPI\Client\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `removeParticipantFromGroup()`

```php
removeParticipantFromGroup($manage_participant_request): \OpenAPI\Client\Model\ManageParticipantResponse
```

Remove participants from group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');



$apiInstance = new OpenAPI\Client\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client()
);
$manage_participant_request = new \OpenAPI\Client\Model\ManageParticipantRequest(); // \OpenAPI\Client\Model\ManageParticipantRequest

try {
    $result = $apiInstance->removeParticipantFromGroup($manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->removeParticipantFromGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **manage_participant_request** | [**\OpenAPI\Client\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\OpenAPI\Client\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

No authorization required

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
