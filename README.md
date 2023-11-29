# airbnb London September 2023
Data set for Analysis. I must elaborate 10 questions, answer them in a python notebook.

## Files description

### Calendar

|Field|Type|Calculated|Description|Reference|
|-----|----|----------|-----------|---------|
|listing_id||| ||
|date|datetime||The date in the listing's calendar||
|available|boolean||Whether the date is available for a booking||
|price|currency||The price listed for the day||
|adjusted_price|currency|| ||
|minimum_nights|integer||Minimum nights for a booking made on this day ||
|maximum_nights|integer||Maximum nights for a booking made on this day ||

Shape (32 100 364, 7)
### Reviews

|Field|Description|
|-----|-----------|
|listing_id| |
|id| |
|date| |
|reviewer_id| |
|reviewer_name| |
|comments| |
Shape (1 581 034, 6)

### Reviews_summary

|Field|Description|
|-----|-----------|
|listing_id| |
|date| |

Shape (1 581 034, 2)

### Listings

shape (195 303, 74)

|Field |Description |
|------|------------|
|id| |
|listing_url| |
|scrape_id| |
|last_scraped| |
|source| |
|name| |
|description| |
|neighborhood_overview| |
|picture_url| |
|host_id| |
|host_url| |
|host_name| |
|host_since| |
|host_location| |
|host_about| |
|host_response_time| |
|host_response_rate| |
|host_acceptance_rate| |
|host_is_superhost| |
|host_thumbnail_url| |
|host_picture_url| |
|host_neighbourhood| |
|host_listings_count| |
|host_total_listings_count| |
|host_verifications| |
|host_has_profile_pic| |
|host_identity_verified| |
|neighbourhood| |
|neighbourhood_cleansed| |
|neighbourhood_group_cleansed| |
|latitude| |
|longitude| |
|property_type| |
|room_type| |
|accommodates| |
|bathrooms| |
|bathrooms_text| |
|bedrooms| |
|beds| |
|amenities| |
|price| |
|minimum_nights| |
|maximum_nights| |
|minimum_minimum_nights| |
|maximum_minimum_nights| |
|minimum_maximum_nights| |
|maximum_maximum_nights| |
|minimum_nights_avg_ntm| |
|maximum_nights_avg_ntm| |
|calendar_updated| |
|has_availability| |
|availability_30| |
|availability_60| |
|availability_90| |
|availability_365| |
|calendar_last_scraped| |
|number_of_reviews| |
|number_of_reviews_ltm| |
|number_of_reviews_l30d| |
|first_review| |
|last_review| |
|review_scores_rating| |
|review_scores_accuracy| |
|review_scores_cleanliness| |
|review_scores_checkin| |
|review_scores_communication| |
|review_scores_location| |
|review_scores_value| |
|license| |
|instant_bookable| |
|calculated_host_listings_count| |
|calculated_host_listings_count_entire_homes| |
|calculated_host_listings_count_private_rooms| |
|calculated_host_listings_count_shared_rooms| |



### Listings Summary

shape (87 947, 1)
|Field|Type|Calculated|Description|Reference|
|-----|----|----------|-----------|---------|
|id|integer||||
|name|string ||||
|host_id|integer ||||
|host_name|string ||||
|neighbourhood_group|text |y|The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles.||
|neighbourhood|text |y|The neighbourhood as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles.	||
|latitude|numeric ||Uses the World Geodetic System (WGS84) projection for latitude and longitude.||
|longitude|numeric ||Uses the World Geodetic System (WGS84) projection for latitude and longitude.||
|room_type|string ||||
|price|currency ||daily price in local currency. Note, $ sign may be used despite locale||
|minimum_nights|integer ||minimum number of night stay for the listing (calendar rules may be different)	||
|number_of_reviews|integer ||The number of reviews the listing has	||
|last_review|date |y|The date of the last/newest review	||
|reviews_per_month| ||||
|calculated_host_listings_count|integer ||The number of listings the host has in the current scrape, in the city/region geography.||
|availability_365|integer |y|avaliability_x. The availability of the listing x days in the future as determined by the calendar. Note a listing may be available because it has been booked by a guest or blocked by the host.	||
|number_of_reviews_ltm|integer |y|The number of reviews the listing has (in the last 12 months)	||
|license|string ||||




	
