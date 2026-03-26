# SdkWhatsappWebMultiDevice\GroupApi

Group setting

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**addParticipantToGroup()**](GroupApi.md#addParticipantToGroup) | **POST** /group/participants | Adding more participants to group |
| [**approveGroupParticipantRequest()**](GroupApi.md#approveGroupParticipantRequest) | **POST** /group/participant-requests/approve | Approve participant request to join group |
| [**createGroup()**](GroupApi.md#createGroup) | **POST** /group | Create group and add participant |
| [**demoteParticipantToMember()**](GroupApi.md#demoteParticipantToMember) | **POST** /group/participants/demote | Demote participants to member |
| [**exportGroupParticipants()**](GroupApi.md#exportGroupParticipants) | **GET** /group/participants/export | Export group participants as CSV |
| [**getGroupInfoFromLink()**](GroupApi.md#getGroupInfoFromLink) | **GET** /group/info-from-link | Get group information from invitation link |
| [**getGroupParticipantRequests()**](GroupApi.md#getGroupParticipantRequests) | **GET** /group/participant-requests | Get list of participant requests to join group |
| [**getGroupParticipants()**](GroupApi.md#getGroupParticipants) | **GET** /group/participants | Get list of participants in a group |
| [**groupInfo()**](GroupApi.md#groupInfo) | **GET** /group/info | Group Info |
| [**groupInviteLink()**](GroupApi.md#groupInviteLink) | **GET** /group/invite-link | Group Invite Link |
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
addParticipantToGroup($x_device_id, $manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

try {
    $result = $apiInstance->addParticipantToGroup($x_device_id, $manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->addParticipantToGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
approveGroupParticipantRequest($x_device_id, $approve_group_participant_request_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$approve_group_participant_request_request = new \SdkWhatsappWebMultiDevice\Model\ApproveGroupParticipantRequestRequest(); // \SdkWhatsappWebMultiDevice\Model\ApproveGroupParticipantRequestRequest

try {
    $result = $apiInstance->approveGroupParticipantRequest($x_device_id, $approve_group_participant_request_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->approveGroupParticipantRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
createGroup($x_device_id, $create_group_request): \SdkWhatsappWebMultiDevice\Model\CreateGroupResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$create_group_request = new \SdkWhatsappWebMultiDevice\Model\CreateGroupRequest(); // \SdkWhatsappWebMultiDevice\Model\CreateGroupRequest

try {
    $result = $apiInstance->createGroup($x_device_id, $create_group_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->createGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
demoteParticipantToMember($x_device_id, $manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

try {
    $result = $apiInstance->demoteParticipantToMember($x_device_id, $manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->demoteParticipantToMember: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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

## `exportGroupParticipants()`

```php
exportGroupParticipants($group_id, $x_device_id): \SplFileObject
```

Export group participants as CSV

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
$group_id = 120363024512399999@g.us; // string | The group ID to export participants for
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->exportGroupParticipants($group_id, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->exportGroupParticipants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID to export participants for | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

**\SplFileObject**

### Authorization

[basicAuth](../../README.md#basicAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/csv`, `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getGroupInfoFromLink()`

```php
getGroupInfoFromLink($link, $x_device_id): \SdkWhatsappWebMultiDevice\Model\GroupInfoFromLinkResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->getGroupInfoFromLink($link, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->getGroupInfoFromLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **link** | **string**| WhatsApp group invitation link | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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
getGroupParticipantRequests($group_id, $x_device_id): \SdkWhatsappWebMultiDevice\Model\GroupParticipantRequestListResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->getGroupParticipantRequests($group_id, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->getGroupParticipantRequests: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID to get participant requests for | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

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

## `getGroupParticipants()`

```php
getGroupParticipants($group_id, $x_device_id): \SdkWhatsappWebMultiDevice\Model\GroupParticipantsResponse
```

Get list of participants in a group

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
$group_id = 120363024512399999@g.us; // string | The group ID to fetch participants for
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.

try {
    $result = $apiInstance->getGroupParticipants($group_id, $x_device_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->getGroupParticipants: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID to fetch participants for | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GroupParticipantsResponse**](../Model/GroupParticipantsResponse.md)

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
groupInfo($x_device_id, $group_id): \SdkWhatsappWebMultiDevice\Model\GroupInfoResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$group_id = 120363025982934543@g.us; // string | WhatsApp Group ID

try {
    $result = $apiInstance->groupInfo($x_device_id, $group_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->groupInfo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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

## `groupInviteLink()`

```php
groupInviteLink($group_id, $x_device_id, $reset): \SdkWhatsappWebMultiDevice\Model\GetGroupInviteLinkResponse
```

Group Invite Link

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
$group_id = 'group_id_example'; // string | WhatsApp Group ID
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$reset = false; // bool | Reset existing invite link

try {
    $result = $apiInstance->groupInviteLink($group_id, $x_device_id, $reset);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->groupInviteLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| WhatsApp Group ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
| **reset** | **bool**| Reset existing invite link | [optional] [default to false] |

### Return type

[**\SdkWhatsappWebMultiDevice\Model\GetGroupInviteLinkResponse**](../Model/GetGroupInviteLinkResponse.md)

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
joinGroupWithLink($x_device_id, $join_group_with_link_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$join_group_with_link_request = new \SdkWhatsappWebMultiDevice\Model\JoinGroupWithLinkRequest(); // \SdkWhatsappWebMultiDevice\Model\JoinGroupWithLinkRequest

try {
    $result = $apiInstance->joinGroupWithLink($x_device_id, $join_group_with_link_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->joinGroupWithLink: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
leaveGroup($x_device_id, $leave_group_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$leave_group_request = new \SdkWhatsappWebMultiDevice\Model\LeaveGroupRequest(); // \SdkWhatsappWebMultiDevice\Model\LeaveGroupRequest

try {
    $result = $apiInstance->leaveGroup($x_device_id, $leave_group_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->leaveGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
promoteParticipantToAdmin($x_device_id, $manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

try {
    $result = $apiInstance->promoteParticipantToAdmin($x_device_id, $manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->promoteParticipantToAdmin: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
rejectGroupParticipantRequest($x_device_id, $reject_group_participant_request_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$reject_group_participant_request_request = new \SdkWhatsappWebMultiDevice\Model\RejectGroupParticipantRequestRequest(); // \SdkWhatsappWebMultiDevice\Model\RejectGroupParticipantRequestRequest

try {
    $result = $apiInstance->rejectGroupParticipantRequest($x_device_id, $reject_group_participant_request_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->rejectGroupParticipantRequest: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
removeParticipantFromGroup($x_device_id, $manage_participant_request): \SdkWhatsappWebMultiDevice\Model\ManageParticipantResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$manage_participant_request = new \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest(); // \SdkWhatsappWebMultiDevice\Model\ManageParticipantRequest

try {
    $result = $apiInstance->removeParticipantFromGroup($x_device_id, $manage_participant_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->removeParticipantFromGroup: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
setGroupAnnounce($x_device_id, $set_group_announce_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$set_group_announce_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupAnnounceRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupAnnounceRequest

try {
    $result = $apiInstance->setGroupAnnounce($x_device_id, $set_group_announce_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupAnnounce: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
setGroupLocked($x_device_id, $set_group_locked_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$set_group_locked_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupLockedRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupLockedRequest

try {
    $result = $apiInstance->setGroupLocked($x_device_id, $set_group_locked_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupLocked: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
setGroupName($x_device_id, $set_group_name_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$set_group_name_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupNameRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupNameRequest

try {
    $result = $apiInstance->setGroupName($x_device_id, $set_group_name_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupName: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
setGroupPhoto($group_id, $x_device_id, $photo): \SdkWhatsappWebMultiDevice\Model\SetGroupPhotoResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$photo = '/path/to/file.txt'; // \SplFileObject | Group photo to upload (JPEG format recommended). Leave empty to remove photo.

try {
    $result = $apiInstance->setGroupPhoto($group_id, $x_device_id, $photo);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupPhoto: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **group_id** | **string**| The group ID | |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
setGroupTopic($x_device_id, $set_group_topic_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
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
$x_device_id = my-device-id; // string | Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as `device_id` query parameter.
$set_group_topic_request = new \SdkWhatsappWebMultiDevice\Model\SetGroupTopicRequest(); // \SdkWhatsappWebMultiDevice\Model\SetGroupTopicRequest

try {
    $result = $apiInstance->setGroupTopic($x_device_id, $set_group_topic_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling GroupApi->setGroupTopic: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **x_device_id** | **string**| Device identifier for multi-device support. Required when multiple devices are registered. If only one device is registered, it will be used as the default. Can also be provided as &#x60;device_id&#x60; query parameter. | [optional] |
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
