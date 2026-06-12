# Event

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Event ID. |
**name** | **string** | Event name. |
**slug** | **string** | Event slug. |
**url** | **string** | Event URL on Etkinlik.io. |
**content** | **string** | Event HTML content with detailed information. |
**start** | **\DateTime** | **Deprecated.** Legacy event start in ISO8601 with offset for the event&#39;s &#x60;timezone&#x60; (wall-clock presentation). Still returned for backward compatibility. New integrations must use &#x60;start_r001&#x60; with &#x60;timezone&#x60;. |
**start_r001** | **\DateTime** | Event start instant in UTC (ISO8601). Prefer with &#x60;end_r001&#x60; and &#x60;timezone&#x60; for new integrations. |
**end** | **\DateTime** | **Deprecated.** Legacy event end in ISO8601 with offset for the event&#39;s &#x60;timezone&#x60;. Still returned for backward compatibility. When the event has no scheduled end (&#x60;end_r001&#x60; is null), this value is local &#x60;start&#x60; plus 2 hours. New integrations must use &#x60;end_r001&#x60; with &#x60;timezone&#x60;. |
**end_r001** | **\DateTime** | Actual scheduled end instant in UTC (ISO8601) when available; null when the event has no end time. Prefer with &#x60;start_r001&#x60; for new integrations. | [optional]
**modified_at** | **\DateTime** | Last content or source-data update instant in UTC (ISO8601). Use with &#x60;sort_by&#x3D;updated&#x60; to list recently changed events. |
**timezone** | **string** | IANA timezone identifier for the event (e.g. &#x60;Europe/Istanbul&#x60;). Always present and valid. Use with &#x60;start_r001&#x60; / &#x60;end_r001&#x60; for display in local wall-clock time. |
**is_free** | **bool** | &#x60;true&#x60; if the event is free, otherwise &#x60;false&#x60;. |
**poster_url** | **string** | Event poster image URL. |
**ticket_url** | **string** | Ticket URL when available; otherwise redirects to the event page. |
**phone** | **string** | Contact phone for the event; null when not set. | [optional]
**email** | **string** | Contact email for the event; null when not set. | [optional]
**facebook_url** | **string** | Facebook profile or page for the event; null when not set. | [optional]
**twitter_url** | **string** | Twitter handle or URL for the event; null when not set. | [optional]
**hashtag** | **string** | Hashtag for the event; null when not set. | [optional]
**web_url** | **string** | Website URL for the event; null when not set. | [optional]
**live_url** | **string** | Live stream URL for the event; null when not set. | [optional]
**android_url** | **string** | Android app URL for the event; null when not set. | [optional]
**ios_url** | **string** | iOS app URL for the event; null when not set. | [optional]
**format** | [**\EtkinlikIo\Api\Model\Format**](Format.md) |  |
**category** | [**\EtkinlikIo\Api\Model\Category**](Category.md) |  |
**venue** | [**\EtkinlikIo\Api\Model\Venue**](Venue.md) | **Deprecated.** Legacy venue object; present only when &#x60;venue_type&#x60; is &#x60;VENUE&#x60; (same registered venue as &#x60;venue_data&#x60;). Still returned for backward compatibility. New integrations must use &#x60;venue_type&#x60; and &#x60;venue_data&#x60;. | [optional]
**venue_type** | **string** | Venue type. - VENUE: Registered venue (&#x60;venue_data&#x60; is a Venue object) - ONLINE: Online event (&#x60;venue_data&#x60; is null) - MANUAL: Manually entered venue (&#x60;venue_data&#x60; is a VenueManual object) |
**venue_data** | [**\EtkinlikIo\Api\Model\EventVenueData**](EventVenueData.md) |  | [optional]
**tags** | [**\EtkinlikIo\Api\Model\Tag[]**](Tag.md) | Tags associated with the event. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
