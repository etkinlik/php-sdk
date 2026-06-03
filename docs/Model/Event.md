# Event

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Event ID. | [optional]
**name** | **string** | Event name. | [optional]
**slug** | **string** | Event slug. | [optional]
**url** | **string** | Event URL on Etkinlik.io. | [optional]
**content** | **string** | Event HTML content with detailed information. | [optional]
**start** | **\DateTime** | Event start time in ISO8601 format. | [optional]
**end** | **\DateTime** | Event end time in ISO8601 format. | [optional]
**is_free** | **bool** | &#x60;true&#x60; if the event is free, otherwise &#x60;false&#x60;. | [optional]
**poster_url** | **string** | Event poster image URL. | [optional]
**ticket_url** | **string** | Ticket URL when available; otherwise redirects to the event page. | [optional]
**phone** | **string** | Contact phone for the event. | [optional]
**email** | **string** | Contact email for the event. | [optional]
**facebook_url** | **string** | Facebook profile or page for the event. | [optional]
**twitter_url** | **string** | Twitter handle or URL for the event. | [optional]
**hashtag** | **string** | Hashtag for the event. | [optional]
**web_url** | **string** | Website URL for the event. | [optional]
**live_url** | **string** | Live stream URL for the event. | [optional]
**android_url** | **string** | Android app URL for the event. | [optional]
**ios_url** | **string** | iOS app URL for the event. | [optional]
**format** | [**\EtkinlikIo\Api\EtkinlikIo\Api\Model\Format**](Format.md) |  | [optional]
**category** | [**\EtkinlikIo\Api\EtkinlikIo\Api\Model\Category**](Category.md) |  | [optional]
**venue_type** | **string** | Venue type. - VENUE: Registered venue (&#x60;venue_data&#x60; is a Venue object) - ONLINE: Online event (&#x60;venue_data&#x60; is null) - MANUAL: Manually entered venue (&#x60;venue_data&#x60; is a VenueManual object) | [optional]
**venue_data** | [**\EtkinlikIo\Api\EtkinlikIo\Api\Model\EventVenueData**](EventVenueData.md) |  | [optional]
**tags** | [**\EtkinlikIo\Api\EtkinlikIo\Api\Model\Tag[]**](Tag.md) | Tags associated with the event. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
