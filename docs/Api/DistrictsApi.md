# EtkinlikIo\Api\DistrictsApi

Operations for districts. Districts of a city can be listed.

All URIs are relative to https://etkinlik.io/api/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCityDistricts()**](DistrictsApi.md#listCityDistricts) | **GET** /cities/{id}/districts | List districts by city |


## `listCityDistricts()`

```php
listCityDistricts($id): \EtkinlikIo\Api\EtkinlikIo\Api\Model\District[]
```

List districts by city

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\DistrictsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | City ID whose districts are requested.

try {
    $result = $apiInstance->listCityDistricts($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DistrictsApi->listCityDistricts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| City ID whose districts are requested. | |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\District[]**](../Model/District.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
