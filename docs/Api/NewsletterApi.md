# SdkWhatsappWebMultiDevice\NewsletterApi

All URIs are relative to http://localhost:3000, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**unfollowNewsletter()**](NewsletterApi.md#unfollowNewsletter) | **POST** /newsletter/unfollow | Unfollow newsletter |


## `unfollowNewsletter()`

```php
unfollowNewsletter($unfollow_newsletter_request): \SdkWhatsappWebMultiDevice\Model\GenericResponse
```

Unfollow newsletter

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure HTTP basic authorization: basicAuth
$config = SdkWhatsappWebMultiDevice\Configuration::getDefaultConfiguration()
              ->setUsername('YOUR_USERNAME')
              ->setPassword('YOUR_PASSWORD');


$apiInstance = new SdkWhatsappWebMultiDevice\Api\NewsletterApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$unfollow_newsletter_request = new \SdkWhatsappWebMultiDevice\Model\UnfollowNewsletterRequest(); // \SdkWhatsappWebMultiDevice\Model\UnfollowNewsletterRequest

try {
    $result = $apiInstance->unfollowNewsletter($unfollow_newsletter_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling NewsletterApi->unfollowNewsletter: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **unfollow_newsletter_request** | [**\SdkWhatsappWebMultiDevice\Model\UnfollowNewsletterRequest**](../Model/UnfollowNewsletterRequest.md)|  | [optional] |

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
