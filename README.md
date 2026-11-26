# Airbnb_Dashboard
Airbnb Performance Dashboard

An interactive Power BI report that looks at Airbnb listings, reviews and ratings across 10 major cities, to see where the platform is big, how it grew, and how guests actually feel about their stays.

About this project

I built this dashboard to explore Airbnb's public listing and review data and turn it into something you can click through instead of scrolling a giant spreadsheet. It covers about 280K listings, 182K hosts and 5.3M+ reviews from 10 cities (Paris, New York, Sydney, Rome, Rio de Janeiro, Istanbul, Mexico City, Bangkok, Cape Town and Hong Kong).
This is a practice project. I made it to get better at Power BI (data modeling, DAX and dashboard design), so it's a learning exercise and not a production report.
It's split into three pages: Overview (growth over time), Reviews (market share and ratings by city) and Ratings (reviewer behaviour, seasonality and host trust). It could be useful for anyone curious about short-term rental markets: analysts, travel and hospitality folks, or just people who like poking around data.

Tech stack
Power BI Desktop for building the report and visuals
Power Query for cleaning and shaping the raw data
DAX for the measures and calculated columns (cumulative %, superhost split, review month and so on)
Data modeling with two tables, Listings and Reviews, connected through listing_id (one-to-many) so filters flow between them
.pbix for the working file and .png for the screenshots below

Data source

The data is Airbnb listing and review data for 10 cities. (Add your exact source and link here, e.g. Inside Airbnb, and the date it was scraped.)
There are two tables:

Table	What's in it
Listings	One row per listing: city, district, room/property type, bedrooms, how many people it accommodates, amenities, host details (host ID, acceptance rate, profile pic, identity verified), review scores and so on
Reviews	One row per review: the date and the listing_id it belongs to, plus a month number and month name I added for the seasonality chart
Each listing can have many reviews, so the relationship is Listings (1) → Reviews (many).

Features and highlights
The problem

Airbnb data is huge and messy. Questions like which cities dominate the market?, how did listings grow, and when did it stall? or which cities do guests rate the best? are hard to answer from raw tables. I wanted one place where you could see all of that quickly.

Goal of the dashboard
Show how Airbnb's listings grew (and shrank) over time
Compare cities by market share, reviews and guest ratings
Look at reviewer behaviour and seasonality
Check how much trust signals (verified identity, profile picture) show up among hosts
Walkthrough of the key visuals

Overview page

KPI cards (top): 279,712 listings, 10 cities, 182,024 hosts, 144 property types and 5,373K reviews.
New Listings area/line chart: new listings per year from 2008 to 2021, split into Entire place, Private room, Shared room and Hotel room, with the total shown behind. There's a button above the chart to switch the view.

Reviews page

Market share by city (Pareto chart): listings per city, split into superhost and non-superhost, with a cumulative % line on top. This is where you see that three cities hold almost half of everything.
Room type bars: a quick comparison of hotel rooms vs Airbnb room types.
Ratings by city: a bar chart of average rating per city. There's a "Select the Detail Level" switch (the star and magnifying glass icons) that flips it to a heatmap table with Accuracy, Cleanliness, Location, Communication and Value scores.

Ratings page

Review frequency: how many times each reviewer posted, with a cumulative line.
Seasonality: a ribbon chart of the share of monthly reviews by city (Mexico City, New York, Paris, Rome, Sydney).
Trust shield: hosts split by whether their identity is verified and whether they have a profile picture.
Insights
Growth peaked in 2015. That year had the highest number of new listings. 2016 and 2017 slowed down, partly because local regulations got tighter. Growth picked up again from 2018 until COVID-19 stopped it in 2019 to 2020.
Three cities hold the market. Paris, New York and Sydney make up almost half of all listings and about 48% of all reviews. Paris is on top for both. One possible reason is that hotel rooms there cost around twice as much as Airbnb rooms.
Mexico City and Rio are rated best, around 94.8 and 94.6 overall. Hong Kong (89.7) and Istanbul (91.1) are rated lowest. Across all cities, Cleanliness and Value are the two lowest-scoring categories.
Most reviewers only review once. About 86% wrote a single review and 98.8% wrote three or fewer. One reviewer shows 283 reviews, with the last two on 13 Oct 2020 across two Bangkok listings. That's either a data error or a very busy globe-trotter, and I couldn't tell which.
Seasonality is clear. Paris and Rome get most of their reviews between April and August (European summer travel), while New York goes up in November and December around the holidays.
Hosts are mostly trustworthy on paper. About two-thirds of hosts (66.9%) have both a verified identity and a profile picture. Only 0.3% have neither.
Who can use it
Travel and hospitality teams can spot which cities have the biggest share and which ones guests love most.
Hosts and investors can see where competition is heavy and where quality scores leave room to stand out (cleanliness and value, for example).
Analysts and policy people can look at how regulation and events like COVID showed up in listing growth

Airbnb_dashboard.png






