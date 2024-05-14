# GeminiCommerce\Tokentracker\TokenTrackerApi

All URIs are relative to https://token-tracker.api.gogemini.io, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**tokenTrackerAdjustTokenBalance()**](TokenTrackerApi.md#tokenTrackerAdjustTokenBalance) | **POST** /v1/{tenantId}/adjust_token_balance | AdjustTokenBalance |
| [**tokenTrackerGetTokenBalance()**](TokenTrackerApi.md#tokenTrackerGetTokenBalance) | **POST** /v1/{tenantId}/get_token_balance | GetTokenBalance |
| [**tokenTrackerStripeWebhook()**](TokenTrackerApi.md#tokenTrackerStripeWebhook) | **POST** /v1/stripe/webhook | StripeWebhook |


## `tokenTrackerAdjustTokenBalance()`

```php
tokenTrackerAdjustTokenBalance($tenant_id, $body): \GeminiCommerce\Tokentracker\Model\TokentrackerAdjustTokenBalanceResponse
```

AdjustTokenBalance

Adjust token balance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: standardAuthorization
$config = GeminiCommerce\Tokentracker\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GeminiCommerce\Tokentracker\Api\TokenTrackerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 'tenant_id_example'; // string
$body = new \GeminiCommerce\Tokentracker\Model\TokenTrackerAdjustTokenBalanceRequest(); // \GeminiCommerce\Tokentracker\Model\TokenTrackerAdjustTokenBalanceRequest

try {
    $result = $apiInstance->tokenTrackerAdjustTokenBalance($tenant_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenTrackerApi->tokenTrackerAdjustTokenBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **string**|  | |
| **body** | [**\GeminiCommerce\Tokentracker\Model\TokenTrackerAdjustTokenBalanceRequest**](../Model/TokenTrackerAdjustTokenBalanceRequest.md)|  | |

### Return type

[**\GeminiCommerce\Tokentracker\Model\TokentrackerAdjustTokenBalanceResponse**](../Model/TokentrackerAdjustTokenBalanceResponse.md)

### Authorization

[standardAuthorization](../../README.md#standardAuthorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokenTrackerGetTokenBalance()`

```php
tokenTrackerGetTokenBalance($tenant_id, $body): \GeminiCommerce\Tokentracker\Model\TokentrackerGetTokenBalanceResponse
```

GetTokenBalance

Get token balance

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: standardAuthorization
$config = GeminiCommerce\Tokentracker\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GeminiCommerce\Tokentracker\Api\TokenTrackerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$tenant_id = 'tenant_id_example'; // string
$body = array('key' => new \stdClass); // object

try {
    $result = $apiInstance->tokenTrackerGetTokenBalance($tenant_id, $body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenTrackerApi->tokenTrackerGetTokenBalance: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **tenant_id** | **string**|  | |
| **body** | **object**|  | |

### Return type

[**\GeminiCommerce\Tokentracker\Model\TokentrackerGetTokenBalanceResponse**](../Model/TokentrackerGetTokenBalanceResponse.md)

### Authorization

[standardAuthorization](../../README.md#standardAuthorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `tokenTrackerStripeWebhook()`

```php
tokenTrackerStripeWebhook($body): object
```

StripeWebhook

Stripe webhook

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: standardAuthorization
$config = GeminiCommerce\Tokentracker\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new GeminiCommerce\Tokentracker\Api\TokenTrackerApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \GeminiCommerce\Tokentracker\Model\TokentrackerStripeWebhookRequest(); // \GeminiCommerce\Tokentracker\Model\TokentrackerStripeWebhookRequest

try {
    $result = $apiInstance->tokenTrackerStripeWebhook($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling TokenTrackerApi->tokenTrackerStripeWebhook: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **body** | [**\GeminiCommerce\Tokentracker\Model\TokentrackerStripeWebhookRequest**](../Model/TokentrackerStripeWebhookRequest.md)|  | |

### Return type

**object**

### Authorization

[standardAuthorization](../../README.md#standardAuthorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
