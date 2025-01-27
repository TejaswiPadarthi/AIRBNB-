INTRODUCTION:
Airbnb is a global online marketplace that connects travellers seeking accommodations with hosts offering unique stays or experiences. Founded in 2008, the platform operates as a peer-to-peer network, 
enabling individuals to rent out their spaces or provide tourism experiences. Its business model is built on fostering trust through user reviews, secure payments, and verification systems. By leveraging the principles of the sharing economy,
Airbnb has disrupted traditional hospitality, providing cost-effective and personalized alternatives to hotels. The platform’s innovative approach has redefined travel,
though it faces challenges such as regulatory compliance, market saturation, and competition. Despite these hurdles, Airbnb continues to expand, offering innovative features and partnerships to enhance the user experience.

Data Summary:
1) id: Unique listing id.
2) name: Name of the property.
3) Host_id: Unique identifier for each listed host.
4) Host_name: Name of the host.
5) neighbourhood group: Location
6) neighbourhood: Area
7) latitude: Latitude coordinates
8) longitude: Longitude coordinates
9) room type: Type of room being rented (e.g., Entire home/apt, Private room).
10) price: Price per night for renting the property.
11) minimum nights: Minimum number of nights required for a booking or stay
12) number_of_reviews: Number of reviews written for the listing
13) last review: Date of the most recent review.
14) reviews_per_month: Average number of reviews per month.
15) calculated_host_listings_count: Total no of listings against the host id
16) availability_365: Number of days when listing is available for booking
The goal of this project is to perform Exploratory Data Analysis (EDA) on the Airbnb NYC 2019 dataset. EDA involves examining the dataset to find useful insights and patterns. By
analysing this data, we aim to discover how different factors affect property prices, understand which neighbourhoods are more popular, and identify trends that can be useful for Airbnb hosts and potential guests.

DATA CLEANING:

A) Handling Missing values:
    The dataset was loaded from excel into powerBI.
1.	name column:
•	  The name column contained null values, indicating that names were not provided for certain records.
•	  To address this, the missing values were replaced with the placeholder value "Unknown".
•	  This ensured consistency in the dataset and allowed for accurate analysis without losing any records due to missing data.
B) host_name column:
•	  The host_name column contained null values, indicating that names were not provided for certain records.
•	  To address this, the missing values were replaced with the placeholder value "Unknown".
•	  This ensured consistency in the dataset and allowed for accurate analysis without losing any records due to missing data.
C) reviews_per_month:
•	  The reviews_per_month column contained null values.
•	  Upon analysis, it was observed that the corresponding values in the number of _reviews column were 0 for these null entries.
•  	Based on this observation, it was concluded that filling the null values in the reviews_per_month column with 0 was the most appropriate approach.
•	  This ensures the data remains consistent and accurately represents the lack of reviews for those entries.

D)	Removed Columns:
    The following columns were removed from the dataset as they were deemed irrelevant for the analysis:
1.	latitude
2.	longitude
3.	last_review

These columns were not directly contributing to the objectives of the analysis and were excluded to simplify the dataset and focus on the relevant variables.

E)	Added Columns:
•	A new column named Revenue was added to the dataset.
•	The Revenue column was calculated based on the values in the Price and Minimum Nights columns using the formula:
•	Revenue = Price × Minimum Nights.
•	This addition helps in analysing the potential earnings for each listing and provides a more comprehensive understanding of the dataset.

Data Visualization:
1) Number of Listings in Each Neighbourhood Group:
   INSIGHTS:
1) Manhattan and Brooklyn: These two neighbourhoods dominate in terms of listing counts, indicating their popularity as Airbnb destinations. These areas likely offer attractions, amenities, and a higher demand for short-term rentals.
2) Staten Island: With the least number of listings, it appears less attractive to hosts, possibly due to fewer tourist attractions or limited demand for short-term rentals.
   
2) Room Type Distribution:
   INSIGHTS:
   •	Entire Home/Apt: 51.97% of listings, indicating that hosts prefer to offer entire properties as rentals. This could be due to the higher potential earnings from renting out full units.
   •	Private Room: 45.66% of listings, showing that a significant portion of hosts choose to rent private rooms within their properties.
   •	Shared Room: 2.37% of listings, a much smaller share, likely due to the reduced appeal of shared accommodations compared to private or entire units.

3)  Top 10 host names:
    INSIGHTS:
    •	Michael has the highest number of listings, followed by David and Sonder. This shows that these hosts have a significant presence in the NYC Airbnb market,
    either through owning multiple properties or managing numerous listings. Their dominance suggests a well-established hosting operation and could reflect their market strategy.


4) Top 10 neighbourhoods:
   INSIGHTS:
Williamsburg and Bedford-Stuyvesant lead in listings, indicating their popularity as neighbourhood choices for Airbnb hosts. 
These neighbourhoods likely have a high demand for short-term rentals, possibly due to their proximity to popular tourist spots or vibrant local culture.
Neighbourhood popularity suggests that hosts in these areas benefit from a steady stream of visitors.

5) Top 10 neighbourhoods based on revenue:
   INSIGHTS:
   Midtown generates the highest revenue, followed by Williamsburg and Harlem. This indicates that properties in Midtown command higher prices and occupancy rates,
   making it a lucrative location for hosts. Premium pricing and the area's central location likely contribute to the high revenue generation.
   Hosts in these neighbourhoods should focus on maintaining quality listings to maximize earnings.

6) Count of price by neighbourhood group and price category:
   INSIGHTS:
   Manhattan and Brooklyn dominate in all price categories (Low, Medium, High), with most listings falling under the Medium price category.
   This shows that while hosts offer a variety of price points, the bulk of listings are positioned in the mid-range, possibly catering to a wide demographic of tourists.
   This trend can be useful for understanding pricing strategies in different neighbourhoods.

7) Category Plot Between Room Type and Neighbourhood Group:
   INSIGHTS:
   Entire Home/Apt dominates across all neighbourhoods, especially in Manhattan and Brooklyn, where the demand for full-property rentals is high.
   This suggests that hosts in these neighbourhoods focus on providing more premium, independent accommodations rather than shared spaces, which aligns with trends in higher-end travel and tourism.

8) Top 5 Average Revenue by Neighbourhood group:
    INSIGHTS:
  Manhattan listings yield the highest average revenue per listing, showing that this area is the most lucrative for hosts. The area' demand for high-end listings and tourism likely contributes to this trend.
  Staten Island, with the lowest average revenue, suggests that it may not attract the same level of demand or premium pricing.

9) Top revenue generate listings:
    INSIGHTS:
   •	Luxury properties such as the "Luxury Triplex Penthouse" and "Furnished Private Room" generate the highest revenue,
   emphasizing that high-end accommodations attract a premium price. These listings contribute significantly to the total revenue and highlight the demand for upscale, unique Airbnb offerings.
   
CONCLUSION:
1) The analysis of the Airbnb NYC 2019 data uncovered significant patterns in pricing,
room types, and popular neighbourhoods, which are critical for understanding market
dynamics.
2)  It highlighted areas and room types with the highest demand, providing insights for
hosts and Airbnb to optimize offerings based on customer preferences.
3) Pricing trends identified through the analysis allow hosts to set competitive rates that
attract more guests while ensuring profitability.
4) The data on room preferences, such as the demand for entire homes versus shared
spaces, helps hosts tailor their listings to meet specific guest needs and preferences.
5) Popular neighbourhoods emerged as key areas for focusing efforts on improving
services, amenities, and guest experiences to maintain a strong presence.
6) Seasonal trends identified when demand is higher or lower, providing valuable
guidance for planning promotions, pricing adjustments, and marketing strategies.
7) This information can help Airbnb and hosts better align their offerings with market
demand, increasing bookings and customer satisfaction.
8) The insights support strategic decision-making, such as where to invest in property
expansion or where to adjust pricing models based on neighbourhood and seasonal
trends.
9) The data-driven insights help Airbnb stay competitive in New York City by ensuring
that the platform meets customer expectations while capitalizing on demand
fluctuations.
10) Understanding these trends allows Airbnb to maintain its leadership in the market,
adapting to evolving guest preferences and competitive pressures.







