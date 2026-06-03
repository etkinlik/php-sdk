# EtkinlikIo\Api\VenuesApi

Operations for listing and retrieving venues in the system. You can fetch the venue catalog and individual venue details.

All URIs are relative to https://etkinlik.io/api/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getVenue()**](VenuesApi.md#getVenue) | **GET** /venues/{id} | Venue detail |
| [**listVenues()**](VenuesApi.md#listVenues) | **GET** /venues | List venues |


## `getVenue()`

```php
getVenue($id): \EtkinlikIo\Api\EtkinlikIo\Api\Model\Venue
```

Venue detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\VenuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Venue ID.

try {
    $result = $apiInstance->getVenue($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VenuesApi->getVenue: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Venue ID. | |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\Venue**](../Model/Venue.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listVenues()`

```php
listVenues($city_ids, $district_ids, $neighborhood_ids, $status_ids, $skip, $take): \EtkinlikIo\Api\EtkinlikIo\Api\Model\PaginatedVenues
```

List venues

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\VenuesApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$city_ids = 'city_ids_example'; // string | Filter records by city IDs. Use comma-separated values for multiple IDs.
$district_ids = 'district_ids_example'; // string | Filter records by district IDs. Use comma-separated values for multiple IDs.
$neighborhood_ids = 'neighborhood_ids_example'; // string | Filter records by neighborhood IDs. Use comma-separated values for multiple IDs.
$status_ids = 'status_ids_example'; // string | Use 1 for approved, 0 for pending. By default all statuses are returned.
$skip = 0; // int | Offset for pagination.
$take = 50; // int | Maximum number of results to return.

try {
    $result = $apiInstance->listVenues($city_ids, $district_ids, $neighborhood_ids, $status_ids, $skip, $take);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling VenuesApi->listVenues: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **city_ids** | **string**| Filter records by city IDs. Use comma-separated values for multiple IDs. | [optional] |
| **district_ids** | **string**| Filter records by district IDs. Use comma-separated values for multiple IDs. | [optional] |
| **neighborhood_ids** | **string**| Filter records by neighborhood IDs. Use comma-separated values for multiple IDs. | [optional] |
| **status_ids** | **string**| Use 1 for approved, 0 for pending. By default all statuses are returned. | [optional] |
| **skip** | **int**| Offset for pagination. | [optional] [default to 0] |
| **take** | **int**| Maximum number of results to return. | [optional] [default to 50] |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\PaginatedVenues**](../Model/PaginatedVenues.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
