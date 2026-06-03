# EtkinlikIo\Api\CitiesApi

Operations for cities. Cities can be listed.

All URIs are relative to https://etkinlik.io/api/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**listCities()**](CitiesApi.md#listCities) | **GET** /cities | List cities |


## `listCities()`

```php
listCities(): \EtkinlikIo\Api\EtkinlikIo\Api\Model\City[]
```

List cities

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\CitiesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);

try {
    $result = $apiInstance->listCities();
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CitiesApi->listCities: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\City[]**](../Model/City.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
