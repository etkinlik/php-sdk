# EtkinlikIo\Api\EventsApi

Operations for listing and retrieving events in the system. You can fetch the event catalog and individual event details.

All URIs are relative to https://etkinlik.io/api/v2, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**getEvent()**](EventsApi.md#getEvent) | **GET** /events/{id} | Event detail |
| [**listEvents()**](EventsApi.md#listEvents) | **GET** /events | List events |
| [**recordEventImpression()**](EventsApi.md#recordEventImpression) | **POST** /events/{id}/impressions | Record event impression |


## `getEvent()`

```php
getEvent($id): \EtkinlikIo\Api\EtkinlikIo\Api\Model\Event
```

Event detail

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Event ID.

try {
    $result = $apiInstance->getEvent($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->getEvent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Event ID. | |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\Event**](../Model/Event.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listEvents()`

```php
listEvents($format_ids, $category_ids, $venue_ids, $city_ids, $start_gte, $end_lte, $sort_by, $skip, $take): \EtkinlikIo\Api\EtkinlikIo\Api\Model\PaginatedEvents
```

List events

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$format_ids = 'format_ids_example'; // string | Filter events by format IDs. Use comma-separated values for multiple IDs.
$category_ids = 'category_ids_example'; // string | Filter events by category IDs. Use comma-separated values for multiple IDs.
$venue_ids = 'venue_ids_example'; // string | Filter events by venue IDs. Use comma-separated values for multiple IDs.
$city_ids = 'city_ids_example'; // string | Filter records by city IDs. Use comma-separated values for multiple IDs.
$start_gte = 'start_gte_example'; // string | Filter events by start time (greater than or equal). Valid datetime, e.g. YYYY-MM-DD HH:mm:ss.
$end_lte = 'end_lte_example'; // string | Filter events by end time (less than or equal). Valid datetime, e.g. YYYY-MM-DD HH:mm:ss.
$sort_by = 'upcoming'; // string | Sort order (case-insensitive). `upcoming`: upcoming events by start time ascending (default). `recent`: most recently added approved events.
$skip = 0; // int | Offset for pagination.
$take = 50; // int | Maximum number of results to return.

try {
    $result = $apiInstance->listEvents($format_ids, $category_ids, $venue_ids, $city_ids, $start_gte, $end_lte, $sort_by, $skip, $take);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->listEvents: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **format_ids** | **string**| Filter events by format IDs. Use comma-separated values for multiple IDs. | [optional] |
| **category_ids** | **string**| Filter events by category IDs. Use comma-separated values for multiple IDs. | [optional] |
| **venue_ids** | **string**| Filter events by venue IDs. Use comma-separated values for multiple IDs. | [optional] |
| **city_ids** | **string**| Filter records by city IDs. Use comma-separated values for multiple IDs. | [optional] |
| **start_gte** | **string**| Filter events by start time (greater than or equal). Valid datetime, e.g. YYYY-MM-DD HH:mm:ss. | [optional] |
| **end_lte** | **string**| Filter events by end time (less than or equal). Valid datetime, e.g. YYYY-MM-DD HH:mm:ss. | [optional] |
| **sort_by** | **string**| Sort order (case-insensitive). &#x60;upcoming&#x60;: upcoming events by start time ascending (default). &#x60;recent&#x60;: most recently added approved events. | [optional] [default to &#39;upcoming&#39;] |
| **skip** | **int**| Offset for pagination. | [optional] [default to 0] |
| **take** | **int**| Maximum number of results to return. | [optional] [default to 50] |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\PaginatedEvents**](../Model/PaginatedEvents.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `recordEventImpression()`

```php
recordEventImpression($id, $event_impression_request): \EtkinlikIo\Api\EtkinlikIo\Api\Model\EventImpressionCreated
```

Record event impression

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure API key authorization: apiKey
$config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKey('X-Etkinlik-Token', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = EtkinlikIo\Api\Configuration::getDefaultConfiguration()->setApiKeyPrefix('X-Etkinlik-Token', 'Bearer');


$apiInstance = new EtkinlikIo\Api\Api\EventsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = 56; // int | Event ID.
$event_impression_request = new \EtkinlikIo\Api\EtkinlikIo\Api\Model\EventImpressionRequest(); // \EtkinlikIo\Api\EtkinlikIo\Api\Model\EventImpressionRequest

try {
    $result = $apiInstance->recordEventImpression($id, $event_impression_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling EventsApi->recordEventImpression: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **int**| Event ID. | |
| **event_impression_request** | [**\EtkinlikIo\Api\EtkinlikIo\Api\Model\EventImpressionRequest**](../Model/EventImpressionRequest.md)|  | [optional] |

### Return type

[**\EtkinlikIo\Api\EtkinlikIo\Api\Model\EventImpressionCreated**](../Model/EventImpressionCreated.md)

### Authorization

[apiKey](../../README.md#apiKey)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
