# EventVenueData

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Venue ID. |
**name** | **string** | Venue name. |
**slug** | **string** | Venue slug. |
**about** | **string** | About the venue. |
**lat** | **string** | Latitude component of the location. |
**lng** | **string** | Longitude component of the location. |
**status** | **int** | 0: pending approval 1: approved |
**phone** | **string** | Venue phone number; null when not set. | [optional]
**web_url** | **string** | Venue website URL; null when not set. | [optional]
**facebook_url** | **string** | Venue Facebook URL; null when not set. | [optional]
**twitter_url** | **string** | Venue Twitter URL; null when not set. | [optional]
**city** | [**\EtkinlikIo\Api\Model\City**](City.md) |  |
**district** | [**\EtkinlikIo\Api\Model\District**](District.md) |  |
**neighborhood** | [**\EtkinlikIo\Api\Model\Neighborhood**](Neighborhood.md) | Neighborhood; null when not linked to a registered neighborhood. | [optional]
**address** | **string** | Venue street address. |
**neighborhood_name** | **string** | Neighborhood name (text). |
**district_name** | **string** | District name (text). |
**city_name** | **string** | City name (text). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
