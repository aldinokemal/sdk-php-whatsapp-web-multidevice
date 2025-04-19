# SdkWhatsappWebMultiDevice

This API is used for sending whatsapp via API


## Installation & Usage

### Requirements

PHP 8.1 and later.

### Composer

To install the bindings via [Composer](https://getcomposer.org/), add the following to `composer.json`:

```json
{
  "repositories": [
    {
      "type": "vcs",
      "url": "https://github.com/aldinokemal/sdk-php-whatsapp-web-multidevice.git"
    }
  ],
  "require": {
    "aldinokemal/sdk-php-whatsapp-web-multidevice": "*@dev"
  }
}
```

Then run `composer install`

### Manual Installation

Download the files and include `autoload.php`:

```php
<?php
require_once('/path/to/SdkWhatsappWebMultiDevice/vendor/autoload.php');
```

## Getting Started

Please follow the [installation procedure](#installation--usage) and then run the following:

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

## API Endpoints

All URIs are relative to *http://localhost:3000*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*AppApi* | [**appDevices**](docs/Api/AppApi.md#appdevices) | **GET** /app/devices | Get list connected devices
*AppApi* | [**appLogin**](docs/Api/AppApi.md#applogin) | **GET** /app/login | Login to whatsapp server
*AppApi* | [**appLoginWithCode**](docs/Api/AppApi.md#apploginwithcode) | **GET** /app/login-with-code | Login with pairing code
*AppApi* | [**appLogout**](docs/Api/AppApi.md#applogout) | **GET** /app/logout | Remove database and logout
*AppApi* | [**appReconnect**](docs/Api/AppApi.md#appreconnect) | **GET** /app/reconnect | Reconnecting to whatsapp server
*GroupApi* | [**addParticipantToGroup**](docs/Api/GroupApi.md#addparticipanttogroup) | **POST** /group/participants | Adding more participants to group
*GroupApi* | [**approveGroupParticipantRequest**](docs/Api/GroupApi.md#approvegroupparticipantrequest) | **POST** /group/participant-requests/approve | Approve participant request to join group
*GroupApi* | [**createGroup**](docs/Api/GroupApi.md#creategroup) | **POST** /group | Create group and add participant
*GroupApi* | [**demoteParticipantToMember**](docs/Api/GroupApi.md#demoteparticipanttomember) | **POST** /group/participants/demote | Demote participants to member
*GroupApi* | [**getGroupParticipantRequests**](docs/Api/GroupApi.md#getgroupparticipantrequests) | **GET** /group/participant-requests | Get list of participant requests to join group
*GroupApi* | [**joinGroupWithLink**](docs/Api/GroupApi.md#joingroupwithlink) | **POST** /group/join-with-link | Join group with link
*GroupApi* | [**leaveGroup**](docs/Api/GroupApi.md#leavegroup) | **POST** /group/leave | Leave group
*GroupApi* | [**promoteParticipantToAdmin**](docs/Api/GroupApi.md#promoteparticipanttoadmin) | **POST** /group/participants/promote | Promote participants to admin
*GroupApi* | [**rejectGroupParticipantRequest**](docs/Api/GroupApi.md#rejectgroupparticipantrequest) | **POST** /group/participant-requests/reject | Reject participant request to join group
*GroupApi* | [**removeParticipantFromGroup**](docs/Api/GroupApi.md#removeparticipantfromgroup) | **POST** /group/participants/remove | Remove participants from group
*MessageApi* | [**deleteMessage**](docs/Api/MessageApi.md#deletemessage) | **POST** /message/{message_id}/delete | Delete Message
*MessageApi* | [**reactMessage**](docs/Api/MessageApi.md#reactmessage) | **POST** /message/{message_id}/reaction | Send reaction to message
*MessageApi* | [**readMessage**](docs/Api/MessageApi.md#readmessage) | **POST** /message/{message_id}/read | Mark as read message
*MessageApi* | [**revokeMessage**](docs/Api/MessageApi.md#revokemessage) | **POST** /message/{message_id}/revoke | Revoke Message
*MessageApi* | [**updateMessage**](docs/Api/MessageApi.md#updatemessage) | **POST** /message/{message_id}/update | Edit message by message ID before 15 minutes
*NewsletterApi* | [**unfollowNewsletter**](docs/Api/NewsletterApi.md#unfollownewsletter) | **POST** /newsletter/unfollow | Unfollow newsletter
*SendApi* | [**sendAudio**](docs/Api/SendApi.md#sendaudio) | **POST** /send/audio | Send Audio
*SendApi* | [**sendContact**](docs/Api/SendApi.md#sendcontact) | **POST** /send/contact | Send Contact
*SendApi* | [**sendFile**](docs/Api/SendApi.md#sendfile) | **POST** /send/file | Send File
*SendApi* | [**sendImage**](docs/Api/SendApi.md#sendimage) | **POST** /send/image | Send Image
*SendApi* | [**sendLink**](docs/Api/SendApi.md#sendlink) | **POST** /send/link | Send Link
*SendApi* | [**sendLocation**](docs/Api/SendApi.md#sendlocation) | **POST** /send/location | Send Location
*SendApi* | [**sendMessage**](docs/Api/SendApi.md#sendmessage) | **POST** /send/message | Send Message
*SendApi* | [**sendPoll**](docs/Api/SendApi.md#sendpoll) | **POST** /send/poll | Send Poll / Vote
*SendApi* | [**sendPresence**](docs/Api/SendApi.md#sendpresence) | **POST** /send/presence | Send presence status
*SendApi* | [**sendVideo**](docs/Api/SendApi.md#sendvideo) | **POST** /send/video | Send Video
*UserApi* | [**userAvatar**](docs/Api/UserApi.md#useravatar) | **GET** /user/avatar | User Avatar
*UserApi* | [**userChangeAvatar**](docs/Api/UserApi.md#userchangeavatar) | **POST** /user/avatar | User Change Avatar
*UserApi* | [**userChangePushName**](docs/Api/UserApi.md#userchangepushname) | **POST** /user/pushname | User Change Push Name
*UserApi* | [**userInfo**](docs/Api/UserApi.md#userinfo) | **GET** /user/info | User Info
*UserApi* | [**userMyContacts**](docs/Api/UserApi.md#usermycontacts) | **GET** /user/my/contacts | Get list of user contacts
*UserApi* | [**userMyGroups**](docs/Api/UserApi.md#usermygroups) | **GET** /user/my/groups | User My List Groups
*UserApi* | [**userMyNewsletter**](docs/Api/UserApi.md#usermynewsletter) | **GET** /user/my/newsletters | User My List Groups
*UserApi* | [**userMyPrivacy**](docs/Api/UserApi.md#usermyprivacy) | **GET** /user/my/privacy | User My Privacy Setting

## Models

- [ApproveGroupParticipantRequestRequest](docs/Model/ApproveGroupParticipantRequestRequest.md)
- [CreateGroupRequest](docs/Model/CreateGroupRequest.md)
- [CreateGroupResponse](docs/Model/CreateGroupResponse.md)
- [CreateGroupResponseResults](docs/Model/CreateGroupResponseResults.md)
- [DeviceResponse](docs/Model/DeviceResponse.md)
- [DeviceResponseResultsInner](docs/Model/DeviceResponseResultsInner.md)
- [ErrorBadRequest](docs/Model/ErrorBadRequest.md)
- [ErrorInternalServer](docs/Model/ErrorInternalServer.md)
- [GenericResponse](docs/Model/GenericResponse.md)
- [Group](docs/Model/Group.md)
- [GroupParticipantRequestListResponse](docs/Model/GroupParticipantRequestListResponse.md)
- [GroupParticipantRequestListResponseResults](docs/Model/GroupParticipantRequestListResponseResults.md)
- [GroupParticipantRequestListResponseResultsDataInner](docs/Model/GroupParticipantRequestListResponseResultsDataInner.md)
- [GroupResponse](docs/Model/GroupResponse.md)
- [GroupResponseResults](docs/Model/GroupResponseResults.md)
- [JoinGroupWithLinkRequest](docs/Model/JoinGroupWithLinkRequest.md)
- [LeaveGroupRequest](docs/Model/LeaveGroupRequest.md)
- [LoginResponse](docs/Model/LoginResponse.md)
- [LoginResponseResults](docs/Model/LoginResponseResults.md)
- [LoginWithCodeResponse](docs/Model/LoginWithCodeResponse.md)
- [LoginWithCodeResponseResults](docs/Model/LoginWithCodeResponseResults.md)
- [ManageParticipantRequest](docs/Model/ManageParticipantRequest.md)
- [ManageParticipantResponse](docs/Model/ManageParticipantResponse.md)
- [ManageParticipantResponseResultsInner](docs/Model/ManageParticipantResponseResultsInner.md)
- [MyListContacts](docs/Model/MyListContacts.md)
- [MyListContactsResponse](docs/Model/MyListContactsResponse.md)
- [MyListContactsResponseResults](docs/Model/MyListContactsResponseResults.md)
- [Newsletter](docs/Model/Newsletter.md)
- [NewsletterResponse](docs/Model/NewsletterResponse.md)
- [NewsletterResponseResults](docs/Model/NewsletterResponseResults.md)
- [NewsletterState](docs/Model/NewsletterState.md)
- [NewsletterThreadMetadata](docs/Model/NewsletterThreadMetadata.md)
- [NewsletterThreadMetadataDescription](docs/Model/NewsletterThreadMetadataDescription.md)
- [NewsletterThreadMetadataName](docs/Model/NewsletterThreadMetadataName.md)
- [NewsletterThreadMetadataPicture](docs/Model/NewsletterThreadMetadataPicture.md)
- [NewsletterThreadMetadataPreview](docs/Model/NewsletterThreadMetadataPreview.md)
- [NewsletterThreadMetadataSettings](docs/Model/NewsletterThreadMetadataSettings.md)
- [NewsletterThreadMetadataSettingsReactionCodes](docs/Model/NewsletterThreadMetadataSettingsReactionCodes.md)
- [NewsletterViewerMetadata](docs/Model/NewsletterViewerMetadata.md)
- [Participant](docs/Model/Participant.md)
- [ReactMessageRequest](docs/Model/ReactMessageRequest.md)
- [ReadMessageRequest](docs/Model/ReadMessageRequest.md)
- [RejectGroupParticipantRequestRequest](docs/Model/RejectGroupParticipantRequestRequest.md)
- [RevokeMessageRequest](docs/Model/RevokeMessageRequest.md)
- [SendContactRequest](docs/Model/SendContactRequest.md)
- [SendLinkRequest](docs/Model/SendLinkRequest.md)
- [SendLocationRequest](docs/Model/SendLocationRequest.md)
- [SendMessageRequest](docs/Model/SendMessageRequest.md)
- [SendPollRequest](docs/Model/SendPollRequest.md)
- [SendPresenceRequest](docs/Model/SendPresenceRequest.md)
- [SendResponse](docs/Model/SendResponse.md)
- [SendResponseResults](docs/Model/SendResponseResults.md)
- [UnfollowNewsletterRequest](docs/Model/UnfollowNewsletterRequest.md)
- [UpdateMessageRequest](docs/Model/UpdateMessageRequest.md)
- [UserAvatarResponse](docs/Model/UserAvatarResponse.md)
- [UserAvatarResponseResults](docs/Model/UserAvatarResponseResults.md)
- [UserChangePushNameRequest](docs/Model/UserChangePushNameRequest.md)
- [UserGroupResponse](docs/Model/UserGroupResponse.md)
- [UserGroupResponseResults](docs/Model/UserGroupResponseResults.md)
- [UserGroupResponseResultsDataInner](docs/Model/UserGroupResponseResultsDataInner.md)
- [UserGroupResponseResultsDataInnerParticipantsInner](docs/Model/UserGroupResponseResultsDataInnerParticipantsInner.md)
- [UserInfoResponse](docs/Model/UserInfoResponse.md)
- [UserInfoResponseResults](docs/Model/UserInfoResponseResults.md)
- [UserInfoResponseResultsDevicesInner](docs/Model/UserInfoResponseResultsDevicesInner.md)
- [UserPrivacyResponse](docs/Model/UserPrivacyResponse.md)
- [UserPrivacyResponseResults](docs/Model/UserPrivacyResponseResults.md)

## Authorization

Authentication schemes defined for the API:
### basicAuth

- **Type**: HTTP basic authentication

## Tests

To run the tests, use:

```bash
composer install
vendor/bin/phpunit
```

## Author



## About this package

This PHP package is automatically generated by the [OpenAPI Generator](https://openapi-generator.tech) project:

- API version: `5.4.0`
    - Generator version: `7.13.0-SNAPSHOT`
- Build package: `org.openapitools.codegen.languages.PhpClientCodegen`
