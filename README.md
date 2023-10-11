Data Analysis Task With Pandas (Transjakarta Case Analysis)


# PT. Transjakarta Data Analysis
## Introduction
This repository contains data and analysis related to PT. Transjakarta, a public transportation company in Jakarta, Indonesia. The analysis aims to optimize Transjakarta fleet performance and the operational aspects of Transjakarta based on the available dataset. The data analyst's role is to provide recommendations for improving the quality of service and operational efficiency.

## Background
PT. Transjakarta operates various types of public transportation services, including BRT (Bus Rapid Transit), Non BRT, Royal Trans, Mikrotrans, Bus Wisata Terpadu, and Transjabodetabek in the Jakarta area. Continuous improvement through monthly evaluations is crucial to monitor and enhance Transjakarta fleet and operational performance, addressing issues like overcrowding, infrastructure quality, elderly-friendly facilities, and women's safety.

## Problem Statement
The key problem is: "How to optimize Transjakarta fleet performance, facilities, and the operational aspects of Transjakarta?"

## Key Questions
a. Passenger Profile:
What is the gender distribution of Transjakarta users?
What is the age distribution of Transjakarta users?

b. Travel Patterns Based on Passenger Profiles:
Which corridors are frequently used by female passengers?
Which corridors are frequently used by senior passengers?

c. Overall Travel Patterns:
Which corridors or routes are the most frequently used by Transjakarta passengers?

d. Peak Usage Times:
When does the system experience peak usage during a day?

e. Travel Patterns During Peak Times:
Which corridors and stops are frequently used during peak times?

f. Weekend and Holiday Travel Patterns:
How do passenger patterns differ on weekends and holidays?

## Data Understanding
Before diving into analysis, it's essential to understand the dataset. Here's an overview:

The dataset has 22 columns and 37,900 rows.
Data ranges from April 1, 2023, to April 30, 2023.
Several columns contain missing data, which will be addressed in the data cleaning process.
Data types are mostly categorical, and some columns need time data type conversion.
No significant anomalies or outliers are detected in the data.

Data Cleaning
a. Data Duplication
No data duplication is found in the dataset.

b. Missing Values
Around 6% of the data contains missing values. Missing values are primarily observed in columns related to corridors, stops, and timestamps.

Missing Value Handling
Missing values are filled through mapping and logic based on specific columns:

Corridor IDs are filled based on corridor names and stop locations (latitude and longitude).
Corridor names are filled based on corridor IDs.
Stop IDs are filled based on stop locations.
Stop names, latitudes, and longitudes are filled based on stop IDs.
Pay amounts are assigned based on corridor types (flat rate or special fare).
Time Data Modification
Timestamp columns 'tapInTime' and 'tapOutTime' are converted to the appropriate data type and separated into hours, days, and weeks for deeper analysis.

c. Data Clean
The dataset is now clean and ready for further analysis.

## Transjakarta Passenger Analysis
In this report, we present an analysis of Transjakarta passenger data with the aim of addressing specific challenges and improving the overall service. The analysis is structured around key problem statements to provide precise insights.

Table of Contents
1.Profile of Transjakarta Passengers
2. Travel Patterns Based on Passenger Profiles
3. Overall Passenger Travel Patterns
4. Busy Hours
5. Travel Patterns During Peak Hours
6. Transjakarta Usage on Weekends and Holidays


### Profile of Transjakarta Passengers
a. Gender-Based Proportions:
- We analyzed the proportion of Transjakarta passengers by gender based on data from the "payCardSex" column. It was assumed that the gender of Transjakarta users corresponds to the gender listed on their pay cards.
- The analysis revealed that female passengers make up a slightly higher percentage (6.6%) than male passengers. While the difference is not substantial, it aligns with Transjakarta's inclusive policies, especially its services for women, aimed at providing safety against sexual harassment. This analysis helps in ensuring that these services cater to the predominant gender demographics effectively.
b. Age Distribution:
- In addition to gender, understanding the age distribution of Transjakarta passengers is essential. This evaluation includes understanding the age groups that might have specific needs and suggesting adjustments to facilities to meet those needs.
- Using birthdate data from the "payCardBirthDate" column, we found that most passengers fall within the age range of 1980-2008, categorizing them as adults and teenagers. While the majority fall into these categories, it's crucial not to overlook the needs of senior citizens and children as per the transport policy guidelines. Although the number of senior citizens using Transjakarta is relatively low, addressing their needs is of high importance.

### Travel Patterns Based on Passenger Profiles
1. Travel Patterns by Gender:
- We assessed which corridors are frequently used by female passengers to identify areas where services like women-only buses might be beneficial.
- As of April 2023, certain corridors are used frequently by female passengers but do not yet have women-only bus services. While these services aren't solely based on the most commonly used corridors by women, it's a valuable consideration when determining which corridors to prioritize for such services.
2. Travel Patterns of Senior Citizens:
- We evaluated the corridors that senior citizens use to inform decisions on improving facilities and services on specific routes.
- Corridors used by senior citizens are analyzed based on which corridors are commonly used, rather than focusing solely on specific bus stops. This approach allows for a more balanced assessment of facility needs.

### Overall Passenger Travel Patterns
1. Heatmaps for Overall Travel Patterns:
Heatmaps visualize the areas most frequented by Transjakarta passengers.
They indicate that passenger usage is concentrated in central Jakarta, particularly Jakarta South. These findings are instrumental in determining the key areas of focus for service improvement and resource allocation.

2. Most Frequently Used Corridors:
- An analysis of the most frequently used corridors by passengers found that corridor 1T, with a route from Cibubur to Balai Kota, has the highest passenger usage. This corridor runs through the business districts of Jakarta.
- Other busy corridors also traverse central Jakarta. Focusing on these corridors is essential for enhancing overall service efficiency.

### Busy Hours
1. Peak Usage Hours in a Day:
- Analysis of the heatmaps categorizes peak hours into "Morning Rush Hour" from 5 am to 9 am, with the peak occurring at 6 am, and "Evening Rush Hour" from 4 pm to 9 pm, with the peak at 5 pm.
- These peak hours are influenced by commuter traffic to and from work, and understanding them is crucial for optimizing service schedules and resources.

### Travel Patterns During Peak Hours
1. Corridors Frequently Used During Peak Hours:
- A closer look at which corridors are busiest during peak hours reveals that Cibubur-Balai Kota remains the most frequently used corridor, followed by others as shown in the provided bar chart.
- It's important to note that these corridors intersect key business and activity areas in Jakarta.

2. Busiest Bus Stops During Peak Hours:
- The analysis of busy bus stops during peak hours aims to support Transjakarta in managing overcrowding at these stops. The data can be used to inform revitalization efforts.

### Transjakarta Usage on Weekends and Holidays
1. Differences in Usage During Holidays:
- Analysis of passenger trends on weekends and during holidays reveals fluctuations in passenger numbers. Weekend usage is generally lower than weekdays, and holidays like Lebaran and collective leaves also experience reduced numbers.
- Despite this, some passengers still use Transjakarta during holidays, especially on weekends. This information can guide resource allocation and the scheduling of buses.

2. Busy Hours on Weekends:
- Analysis of busy hours on weekends during holidays shows that passenger usage is relatively consistent from 5 am to 8 pm. There's no specific peak, indicating that the allocation of resources should be distributed more evenly.

3. Corridors Used on Holidays:
- The corridors frequently used on holidays differ from peak hours on weekends. Passengers tend to use corridors that lead to bus terminals on holidays, particularly during the Lebaran holiday.
This suggests the importance of evaluating the optimal operation of these corridors during holidays to ensure they meet the demand.

## Recommendations

1. Provision of Women-Specific Facilities:
Expand women-only bus services on corridors frequently used by female passengers without adequate facilities. Examples include Pasar Minggu - Tanah Abang, Poris Plawad - Bundaran Senayan, and Rusun Rawa Bebek – Kodamar corridors.

2. Facilities and Services for Seniors:
- Enhance elderly-friendly facilities at bus stops, including priority seating and easily readable information.
Conduct educational campaigns through announcements at bus stops and on buses to encourage passengers to prioritize seniors when using facilities and priority seats.
- Modify the Transjakarta fleet to include more priority seating on routes frequently used by seniors.
- Revitalize bus stops that are challenging for seniors to access.

3. Optimization of Transjakarta Fleet and Facilities on Busy Corridors:
- Increase the number of buses on crowded and frequently problematic corridors like Cibubur-Balai Kota, Ciputat - CSW, and Harmoni - Jakarta International Stadium to address congestion during peak hours.
- Achieve Transjakarta fleet increases by reassigning buses from less crowded corridors to busy ones.
- Ensure that the Transjakarta fleet availability aligns with passenger volumes during peak times.

4. Adjustment of Operational Hours:
- Consider adapting Transjakartas fleet operational hours during peak periods to maintain service quality and prevent overcrowding.

5. Improvement of Facilities and Bus Stop Layout:
- Revitalize and expand bus stops with high passenger volumes, especially at key locations such as Garuda Taman Mini, Rusun Muara Kapuk, Penjaringan, Rawa Selatan, and Cibubur Junction.
- Enhance accessibility and comfort at bus stops that continue to receive complaints from passengers, such as the Senayan bus stop.

6. Transjakarta Fleet Allocation on Weekends and Holidays:
- Allocate or implement a Transjakarta fleet reassignment system for locations frequently visited on weekends, such as city centers, shopping centers, and tourist destinations. In the dataset, these locations are served by routes like Pinang Ranti - Kampung Rambutan, JIS- Terminal Muara Angke, and Pinang Ranti - Bundaran Senayan.
- For Lebaran holidays, focus Transjakarta fleet allocation or reassignment on corridors with terminals like Kampung Melayu, Kampung Rambutan, and Pulo Gadung, as data indicates significant passenger traffic to these areas.
Equitably allocate tourist Transjakarta fleet to accommodate passenger volumes and reduce long waiting times on weekends and holidays.

For a more interactive and visual representation of the analysis, you can access the Tableau dashboard here (https://public.tableau.com/app/profile/eva.fachria/viz/TransjakartaDataAnalysisbyEvaFachria/Story1)

### Author
[EVA FACHRIA]

### Acknowledgments
Special thanks to [Ragil Hadi Prasetyo] for the help and insight.
