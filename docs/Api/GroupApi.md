# SdkWhatsappWebMultiDevice\GroupApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addParticipantToGroup()**](GroupApi.md#addParticipantToGroup) | **POST** /group/participants | Adding more participants to group |
| [**approveGroupParticipantRequest()**](GroupApi.md#approveGroupParticipantRequest) | **POST** /group/participant-requests/approve | Approve participant request to join group |
| [**createGroup()**](GroupApi.md#createGroup) | **POST** /group | Create group and add participant |
| [**demoteParticipantToMember()**](GroupApi.md#demoteParticipantToMember) | **POST** /group/participants/demote | Demote participants to member |
| [**getGroupInfoFromLink()**](GroupApi.md#getGroupInfoFromLink) | **GET** /group/info-from-link | Get group information from invitation link |
| [**getGroupParticipantRequests()**](GroupApi.md#getGroupParticipantRequests) | **GET** /group/participant-requests | Get list of participant requests to join group |
| [**groupInfo()**](GroupApi.md#groupInfo) | **GET** /group/info | Group Info |
| [**joinGroupWithLink()**](GroupApi.md#joinGroupWithLink) | **POST** /group/join-with-link | Join group with link |
| [**leaveGroup()**](GroupApi.md#leaveGroup) | **POST** /group/leave | Leave group |
| [**promoteParticipantToAdmin()**](GroupApi.md#promoteParticipantToAdmin) | **POST** /group/participants/promote | Promote participants to admin |
| [**rejectGroupParticipantRequest()**](GroupApi.md#rejectGroupParticipantRequest) | **POST** /group/participant-requests/reject | Reject participant request to join group |
| [**removeParticipantFromGroup()**](GroupApi.md#removeParticipantFromGroup) | **POST** /group/participants/remove | Remove participants from group |
| [**setGroupAnnounce()**](GroupApi.md#setGroupAnnounce) | **POST** /group/announce | Set group announce mode |
| [**setGroupLocked()**](GroupApi.md#setGroupLocked) | **POST** /group/locked | Set group locked status |
| [**setGroupName()**](GroupApi.md#setGroupName) | **POST** /group/name | Set group name |
| [**setGroupPhoto()**](GroupApi.md#setGroupPhoto) | **POST** /group/photo | Set group photo |
| [**setGroupTopic()**](GroupApi.md#setGroupTopic) | **POST** /group/topic | Set group topic |


## `addParticipantToGroup()`

```php
addParticipantToGroup($manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
```

Adding more participants to group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

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
| **manage_participant_request** | [**\SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `approveGroupParticipantRequest()`

```php
approveGroupParticipantRequest($approve_group_participant_request_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Approve participant request to join group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$approve_group_participant_request_request = new \SdkWhatsappWebMultiDevice\Model\ApproveGroupParticipantRequestRequest(); // \SdkWhatsappWebMultiDevice\Model\ApproveGroupParticipantRequestRequest

try {
    $result = $apiInstance->approveGroupParticipantRequest($approve_group_participant_request_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->approveGroupParticipantRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **approve_group_participant_request_request** | [**\SdkWhatsappWebMultiDevice\Model\ApproveGroupParticipantRequestRequest**](../Model/ApproveGroupParticipantRequestRequest.md)|  | [optional] |

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

## `createGroup()`

```php
createGroup($create_group_request): \SdkWhatsappWebMultiDevice\Model\CreateGroupResponse
```

Create group and add participant

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$create_group_request = new \SdkWhatsappWebMultiDevice\Model\CreateGroupRequest(); // \SdkWhatsappWebMultiDevice\Model\CreateGroupRequest

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
| **create_group_request** | [**\SdkWhatsappWebMultiDevice\Model\CreateGroupRequest**](../Model/CreateGroupRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\CreateGroupResponse**](../Model/CreateGroupResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `demoteParticipantToMember()`

```php
demoteParticipantToMember($manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
```

Demote participants to member

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

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
| **manage_participant_request** | [**\SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupInfoFromLink()`

```php
getGroupInfoFromLink($link): \SdkWhatsappWebMultiDevice\Model\GroupInfoFromLinkResponse
```

Get group information from invitation link

Retrieve group information without joining the group using its invitation link

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$link = https://chat.whatsapp.com/whatsappKeyJoinGroup; // string | WhatsApp group invitation link

try {
    $result = $apiInstance->getGroupInfoFromLink($link);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->getGroupInfoFromLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **link** | **string**| WhatsApp group invitation link | |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GroupInfoFromLinkResponse**](../Model/GroupInfoFromLinkResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupParticipantRequests()`

```php
getGroupParticipantRequests($group_id): \SdkWhatsappWebMultiDevice\Model\GroupParticipantRequestListResponse
```

Get list of participant requests to join group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = 120363024512399999@g.us; // string | The group ID to get participant requests for

try {
    $result = $apiInstance->getGroupParticipantRequests($group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->getGroupParticipantRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID to get participant requests for | |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GroupParticipantRequestListResponse**](../Model/GroupParticipantRequestListResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `groupInfo()`

```php
groupInfo($group_id): \SdkWhatsappWebMultiDevice\Model\GroupInfoResponse
```

Group Info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = 120363025982934543@g.us; // string | WhatsApp Group ID

try {
    $result = $apiInstance->groupInfo($group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->groupInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| WhatsApp Group ID | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GroupInfoResponse**](../Model/GroupInfoResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `joinGroupWithLink()`

```php
joinGroupWithLink($join_group_with_link_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Join group with link

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$join_group_with_link_request = new \SdkWhatsappWebMultiDevice\Model\JoinGroupWithLinkRequest(); // \SdkWhatsappWebMultiDevice\Model\JoinGroupWithLinkRequest

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
| **join_group_with_link_request** | [**\SdkWhatsappWebMultiDevice\Model\JoinGroupWithLinkRequest**](../Model/JoinGroupWithLinkRequest.md)|  | [optional] |

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

## `leaveGroup()`

```php
leaveGroup($leave_group_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Leave group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$leave_group_request = new \SdkWhatsappWebMultiDevice\Model\LeaveGroupRequest(); // \SdkWhatsappWebMultiDevice\Model\LeaveGroupRequest

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
| **leave_group_request** | [**\SdkWhatsappWebMultiDevice\Model\LeaveGroupRequest**](../Model/LeaveGroupRequest.md)|  | [optional] |

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

## `promoteParticipantToAdmin()`

```php
promoteParticipantToAdmin($manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
```

Promote participants to admin

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

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
| **manage_participant_request** | [**\SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `rejectGroupParticipantRequest()`

```php
rejectGroupParticipantRequest($reject_group_participant_request_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Reject participant request to join group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$reject_group_participant_request_request = new \SdkWhatsappWebMultiDevice\Model\RejectGroupParticipantRequestRequest(); // \SdkWhatsappWebMultiDevice\Model\RejectGroupParticipantRequestRequest

try {
    $result = $apiInstance->rejectGroupParticipantRequest($reject_group_participant_request_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->rejectGroupParticipantRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **reject_group_participant_request_request** | [**\SdkWhatsappWebMultiDevice\Model\RejectGroupParticipantRequestRequest**](../Model/RejectGroupParticipantRequestRequest.md)|  | [optional] |

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

## `removeParticipantFromGroup()`

```php
removeParticipantFromGroup($manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
```

Remove participants from group

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

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
| **manage_participant_request** | [**\SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest**](../Model/ManageParticipantRequest.md)|  | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse**](../Model/ManageParticipantResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setGroupAnnounce()`

```php
setGroupAnnounce($set_group_announce_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Set group announce mode

Enable/disable announce mode so only admins can send messages

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$set_group_announce_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupAnnounceRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupAnnounceRequest

try {
    $result = $apiInstance->setGroupAnnounce($set_group_announce_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupAnnounce: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **set_group_announce_request** | [**\SdkWhatsappWebMultiDevice\Model\SetGroupAnnounceRequest**](../Model/SetGroupAnnounceRequest.md)|  | [optional] |

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

## `setGroupLocked()`

```php
setGroupLocked($set_group_locked_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Set group locked status

Lock/unlock group so only admins can modify group info

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$set_group_locked_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupLockedRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupLockedRequest

try {
    $result = $apiInstance->setGroupLocked($set_group_locked_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupLocked: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **set_group_locked_request** | [**\SdkWhatsappWebMultiDevice\Model\SetGroupLockedRequest**](../Model/SetGroupLockedRequest.md)|  | [optional] |

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

## `setGroupName()`

```php
setGroupName($set_group_name_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Set group name

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$set_group_name_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupNameRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupNameRequest

try {
    $result = $apiInstance->setGroupName($set_group_name_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **set_group_name_request** | [**\SdkWhatsappWebMultiDevice\Model\SetGroupNameRequest**](../Model/SetGroupNameRequest.md)|  | [optional] |

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

## `setGroupPhoto()`

```php
setGroupPhoto($group_id, $photo): \SdkWhatsappWebMultiDevice\Model\SetGroupPhotoResponse
```

Set group photo

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$group_id = 'group_id_example'; // string | The group ID
$photo = '/path/to/file.txt'; // \SplFileObject | Group photo to upload (JPEG format recommended). Leave empty to remove photo.

try {
    $result = $apiInstance->setGroupPhoto($group_id, $photo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupPhoto: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID | |
| **photo** | **\SplFileObject****\SplFileObject**| Group photo to upload (JPEG format recommended). Leave empty to remove photo. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\SetGroupPhotoResponse**](../Model/SetGroupPhotoResponse.md)

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `setGroupTopic()`

```php
setGroupTopic($set_group_topic_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Set group topic

Set or remove group topic/description

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\GroupApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$set_group_topic_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupTopicRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupTopicRequest

try {
    $result = $apiInstance->setGroupTopic($set_group_topic_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupTopic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **set_group_topic_request** | [**\SdkWhatsappWebMultiDevice\Model\SetGroupTopicRequest**](../Model/SetGroupTopicRequest.md)|  | [optional] |

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
