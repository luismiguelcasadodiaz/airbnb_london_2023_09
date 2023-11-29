# airbnb London September 2023
Data set for Analysis. I must elaborate 10 questions, answer them in a python notebook.

## Steps to solve the puzzle into an ipython notebook

	1.- Ask 10 questions from the dataset and answer them.
 		Make sure 6-7 out of these 10 questions are quantifiable i.e there should be a definite numerical output of that question. 
   		Make sure 3-4 out of these 10 questions could be non-quantifiable questions (For eg: Answering how the price and reviews vary with respect to the type of 
 accommodation, is a non-quantifiable question.)
	2.- Divide your code for each question into 2 parts:
		In 1 block of code do any pre-processing that is required for that question. (cleaning, normalization,  etc.) and generate a clean dataset ready for final analysis.
		In 1 block of code put all the required analysis 

(Step 4) Your analysis will be graded based on
(Step 4.1) Business value of the finding
(Step 4.2) How non-obvious the questions and the insight s  are.
(Step 4.3) Correctness of the questions and answers.
(Step 4.4) Intermediate steps to demonstrate your thought process from questions to answers.
(Step 5) Both positive as well as negative results are interesting to us if you can justify your hypothesis and insights.
(Step 6) You are required to submit the solution as an ipython notebook to ivana.kruhoberec@turing.com

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

|Field|Type|Calculated|Description|Reference|
|-----|----|----------|-----------|---------|
|listing_id| || ||
|id| || ||
|date|datetime || ||
|reviewer_id| || ||
|reviewer_name| || ||
|comments| || ||

Shape (1 581 034, 6)

### Reviews_summary

|Field|Type|Calculated|Description|Reference|
|-----|----|----------|-----------|---------|
|listing_id| || ||
|date|datetime || ||

Shape (1 581 034, 2)

### Listings

shape (195 303, 74)

|Field|Type|Calculated|Description|Reference|
|-----|----|----------|-----------|---------|
|id|integer ||Airbnb's unique identifier for the listing | |
|listing_url|text |y| | |
|scrape_id|bigint |y|Inside Airbnb "Scrape" this was part of | |
|last_scraped|datetime |y|UTC. The date and time this listing was "scraped". | |
|source|text ||One of "neighbourhood search" or "previous scrape". "neighbourhood search" means that the listing was found by searching the city, while "previous scrape" means that the listing was seen in another scrape performed in the last 65 days, and the listing was confirmed to be still available on the Airbnb site | |
|name|text ||Name of the listing | |
|description|text ||Detailed description of the listing | |
|neighborhood_overview|text ||Host's description of the neighbourhood | |
|picture_url|text ||URL to the Airbnb hosted regular sized image for the listing| |
|host_id|integer ||Airbnb's unique identifier for the host/user | |
|host_url|text || The Airbnb page for the host| |
|host_name|text ||Name of the host. Usually just the first name(s)| |
|host_since|date ||The date the host/user was created. For hosts that are Airbnb guests this could be the date they registered as a guest. | |
|host_location|text || The host's self reported location| |
|host_about|text || Description about the host| |
|host_response_time| || | |
|host_response_rate| || | |
|host_acceptance_rate| ||That rate at which a host accepts booking requests. | |
|host_is_superhost|boolean || | |
|host_thumbnail_url|text || | |
|host_picture_url|text || | |
|host_neighbourhood|text || | |
|host_listings_count|text ||The number of listings the host has (per Airbnb calculations) | |
|host_total_listings_count|text ||The number of listings the host has (per Airbnb calculations) | |
|host_verifications| || | |
|host_has_profile_pic|boolean || | |
|host_identity_verified|boolean || | |
|neighbourhood|text || | |
|neighbourhood_cleansed|text |y|The neighbourhood as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. | |
|neighbourhood_group_cleansed|text |y|The neighbourhood group as geocoded using the latitude and longitude against neighborhoods as defined by open or public digital shapefiles. | |
|latitude|numeric || Uses the World Geodetic System (WGS84) projection for latitude and longitude.| |
|longitude|numeric ||Uses the World Geodetic System (WGS84) projection for latitude and longitude. | |
|property_type|text ||Self selected property type. Hotels and Bed and Breakfasts are described as such by their hosts in this field | |
|room_type|text || Entire home/apt\|Private room\|Shared room\|Hotel] <br> All homes are grouped into the following three room types: <br>  <br> Entire place <br> Private room <br> Shared room <br> Entire place <br> Entire places are best if you're seeking a home away from home. With an entire place, you'll have the whole space to yourself. This usually includes a bedroom, a bathroom, a kitchen, and a separate, dedicated entrance. Hosts should note in the description if they'll be on the property or not (ex: "Host occupies first floor of the home"), and provide further details on the listing. <br>  <br> Private rooms <br> Private rooms are great for when you prefer a little privacy, and still value a local connection. When you book a private room, you'll have your own private room for sleeping and may share some spaces with others. You might need to walk through indoor spaces that another host or guest may occupy to get to your room. <br>  <br> Shared rooms <br> Shared rooms are for when you don't mind sharing a space with others. When you book a shared room, you'll be sleeping in a space that is shared with others and share the entire space with other people. Shared rooms are popular among flexible travelers looking for new friends and budget-friendly stays.|[Types of place to stay](https://www.airbnb.com/help/article/5/what-does-the-room-type-of-a-listing-mean) |
|accommodates|integer || The maximum capacity of the listing| |
|bathrooms|numeric ||The number of bathrooms in the listing | |
|bathrooms_text|string||The number of bathrooms in the listing. <br> On the Airbnb web-site, the bathrooms field has evolved from a number to a textual description. For older scrapes, bathrooms is used. | |
|bedrooms|integer ||The number of bedrooms | |
|beds|integer ||The number of bed(s) | |
|amenities|json || | |
|price|currency ||daily price in local currency | |
|minimum_nights|integer ||minimum number of night stay for the listing (calendar rules may be different) | |
|maximum_nights|integer ||maximum number of night stay for the listing (calendar rules may be different) | |
|minimum_minimum_nights|integer |y|the smallest minimum_night value from the calender (looking 365 nights in the future)| |
|maximum_minimum_nights|integer |y|the largest minimum_night value from the calender (looking 365 nights in the future)| |
|minimum_maximum_nights|integer |y|the smallest maximum_night value from the calender (looking 365 nights in the future)| |
|maximum_maximum_nights|integer |y|the largest maximum_night value from the calender (looking 365 nights in the future) | |
|minimum_nights_avg_ntm|numeric |y|the average minimum_night value from the calender (looking 365 nights in the future) | |
|maximum_nights_avg_ntm|numeric |y|the average maximum_night value from the calender (looking 365 nights in the future) | |
|calendar_updated|date || | |
|has_availability|boolean || | |
|availability_30|integer |y|avaliability_x. The availability of the listing 30 days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. | |
|availability_60|integer |y|avaliability_x. The availability of the listing 60 days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. | |
|availability_90|integer |y|avaliability_x. The availability of the listing 90 days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. | |
|availability_365|integer y||avaliability_x. The availability of the listing 365 days in the future as determined by the calendar. Note a listing may not be available because it has been booked by a guest or blocked by the host. | |
|calendar_last_scraped|date || | |
|number_of_reviews|integer ||The number of reviews the listing has | |
|number_of_reviews_ltm|integer |y|The number of reviews the listing has (in the last 12 months) | |
|number_of_reviews_l30d|integer |y| The number of reviews the listing has (in the last 30 days)| |
|first_review|date |y| The date of the first/oldest review| |
|last_review|date |y|The date of the last/newest review ||
|review_scores_rating| || | |
|review_scores_accuracy| || | |
|review_scores_cleanliness| || | |
|review_scores_checkin| || | |
|review_scores_communication| || | |
|review_scores_location| || | |
|review_scores_value| || | |
|license|text ||The licence/permit/registration number | |
|instant_bookable|boolean ||[t=true; f=false]. Whether the guest can automatically book the listing without the host requiring to accept their booking request. An indicator of a commercial listing. | |
|calculated_host_listings_count|integer |y|The number of listings the host has in the current scrape, in the city/region geography. | |
|calculated_host_listings_count_entire_homes|integer |y|The number of Entire home/apt listings the host has in the current scrape, in the city/region geography | |
|calculated_host_listings_count_private_rooms|integer |y|The number of Private room listings the host has in the current scrape, in the city/region geography | |
|calculated_host_listings_count_shared_rooms|integer |y|The number of Shared room listings the host has in the current scrape, in the city/region geography | |
|reviews_per_month|numeric |y|The number of reviews the listing has over the lifetime of the listing | |


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




	
