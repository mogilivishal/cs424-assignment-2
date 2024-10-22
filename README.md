# CS424: Visualization and Visual Analytics - Assignment - 2
# Chicago Traffic Tracker Dataset

## Short Description
The Chicago Traffic Tracker dataset is a comprehensive collection of historical estimated congestion data for over 1,000 traffic segments in Chicago, starting from around March 2018.
This dataset is a valuable resource for understanding traffic conditions on the city's arterial streets and comprises a vast amount of data with 275 million rows and 22 columns of attributes.
The congestion estimates are generated every 10 minutes by continuously monitoring and analyzing GPS traces received from Chicago Transit Authority (CTA) buses.

The dataset offers a wide range of details, including segment length, estimated traffic speed, street names, traffic flow direction, and several other parameters. It is helpful for a range of applications, including traffic management, urban planning, transportation research, and public transit optimization. It also provides congestion estimations at both the segment and regional levels. Researchers, municipal planners, traffic engineers, and transportation businesses can use the information to acquire understanding of Chicago's traffic patterns and make data-driven choices to enhance traffic flow and urban mobility.

**a. Columns in the Dataset:**
The dataset contains 22 columns:

1. **TIME**: Represents date and time.
2. **SEGMENT_ID**: A unique identifier for each traffic segment.
3. **SPEED**: Estimated traffic speed in miles per hour.
4. **STREET**: Street name of the traffic segment.
5. **DIRECTION**: Traffic flow direction for the segment.
6. **FROM_STREET**: Start street for the segment in the direction of traffic flow.
7. **TO_STREET**: End street for the segment in the direction of traffic flow.
8. **LENGTH**: Length of the segment in miles.
9. **STREET_HEADING**: The position of the segment in the address grid.
10. **COMMENTS**: Plain text comments.
11. **BUS_COUNT**: Number of buses providing a GPS feed used to estimate congestion.
12. **MESSAGE_COUNT**: Number of GPS probes received (or used) for estimating the speed for that segment.
13. **HOUR**: Hour of the day.
14. **DAY_OF_WEEK**: Day of the week (Sunday = 1).
15. **MONTH**: Month of the year.
16. **RECORD_ID**: A unique identifier for each record in the dataset.
17. **START_LATITUDE**: Latitude of the start of the segment.
18. **START_LONGITUDE**: Longitude of the start of the segment.
19. **END_LATITUDE**: Latitude of the end of the segment.
20. **END_LONGITUDE**: Longitude of the end of the segment.
21. **START_LOCATION**: Location of the start of the segment.
22. **END_LOCATION**: Location of the end of the segment.

**b. Spatial or Temporal Component:**
- **Spatial Component**: The dataset includes information related to the streets (STREET, DIRECTION, FROM_STREET, TO_STREET) and geographical coordinates (latitude and longitude) for the start and end points of the segments. This suggests a spatial component related to the location of traffic segments in Chicago.

- **Temporal Component**: The dataset contains temporal information, including date and time (TIME), hour of the day (HOUR), day of the week (DAY_OF_WEEK), and month (MONTH). These temporal components indicate a time series aspect to the data.

**c. Categorical and Numerical Columns:**
- **Categorical Columns**: Columns with categorical data include STREET, DIRECTION, FROM_STREET, TO_STREET, STREET_HEADING, COMMENTS, and START_LOCATION/END_LOCATION.
- **Numerical Columns**: Columns with numerical data include SEGMENT_ID, SPEED, LENGTH, BUS_COUNT, MESSAGE_COUNT, HOUR, DAY_OF_WEEK, MONTH, START_LATITUDE, START_LONGITUDE, END_LATITUDE, and END_LONGITUDE.

**d. Specific Focus for Multiple Categories:**
Based on our visualizations we're specifically focusing on categories like HOUR, DAY_OF_WEEK, SPEED, STREET, BUS_COUNT, DIRECTION, LENGTH, MONTH, SEGMENT_ID and LENGTH.

**e. Spatial and Temporal Coverage:**
- **Spatial Coverage**: The data represents traffic segments in Chicago, and the spatial coverage extends to the entire city.
- **Temporal Coverage**: The dataset starts from March 2018 to present. It covers traffic congestion data for multiple years.

**f. Percentage of Missing Values:**
The total percentage of missing values in the dataset is 87.87%

The dataset is a valuable resource for understanding traffic congestion in Chicago and can aid in data-driven decision-making for traffic management and urban planning.

This dataset has records for both Traffic Segments and Traffic Regions. Traffic Segments provide observed speeds for specific segments of streets, while Traffic Regions offer average traffic conditions for larger areas of the city with similar traffic patterns. Traffic congestion can vary widely due to factors like intersections, traffic signals, transit movements, alternative routes, and crashes, leading to fluctuations in speed on individual arterial segments. The dataset is an invaluable tool for monitoring and managing traffic in Chicago's arterial streets.

## Implemented Visualizations

### Visualization 1: Heatmap of Congestion by Hour and Day

![heatmap](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/cbc9740d-eebc-4fa5-ad40-b4ff2aae48f7)


The heatmap visualization of congestion by hour and day provides a comprehensive and insightful view of traffic patterns in Chicago. By using color intensity to represent congestion levels, it allows viewers to quickly grasp when and where congestion is most prevalent.

**Derived Insights:**

- **Peak Congestion Hours:** The heatmap reveals the peak congestion hours in Chicago, which appear to be during the weekday mornings and evenings, particularly between 7 AM and 9 AM and between 4 PM and 6 PM. This information is valuable for commuters who can use it to plan their travel times more efficiently, potentially avoiding heavy traffic.

- **Weekday vs. Weekend:** The heatmap clearly distinguishes between weekdays and weekends. Weekdays exhibit distinct rush-hour patterns, while weekends generally show lower and more consistent congestion levels throughout the day. This insight can be beneficial for both regular commuters and leisure travelers.

- **Midweek Variations:** Thursday appears to have slightly lower congestion during the morning rush hour compared to other weekdays. This could indicate a midweek relief from traffic stress for some commuters.

- **Late-Night and Early-Morning Traffic:** While most congestion occurs during the day, some segments experience late-night and early-morning congestion. This might be attributed to night-shift workers or early morning commuters. Understanding this can help city planners make necessary adjustments to traffic flow and public transportation schedules.

- **Low Congestion Periods:** The late-night and early-morning hours, especially on weekends, show relatively low congestion. This can be useful for those who prefer to travel during quieter times.

- **Consistency of Weekday Patterns:** The rush-hour patterns on weekdays are remarkably consistent throughout the week, suggesting that commuters can rely on this information to plan their daily trips effectively.

In conclusion, the heatmap visualization of congestion by hour and day provides valuable insights into Chicago's traffic conditions. It allows commuters to make informed decisions about when to travel to minimize congestion-related delays. City planners can also utilize this data to improve traffic management during peak hours.


### Visualization 2: Weekly Average Congestion Line Chart

![avg speed](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/997c0763-10ca-48e3-b026-ffc1c8dd0489)

![hour speed](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/6227a2ab-e22b-439b-891e-4b3938f1f3e4)



The Weekly Average Congestion Line Chart provides a clear and insightful representation of how congestion levels change throughout the days of the week. The x-axis displays the days of the week, while the y-axis shows the average congestion levels (in terms of SPEED). 

**Derived Insights:**

- **Weekday Traffic Patterns:** The chart shows distinct patterns between weekdays and weekends. On weekdays, the average congestion is higher, with peak congestion during weekdays, particularly on Thursday and Friday. This information can help commuters plan their workweek routes more efficiently, perhaps considering public transportation or carpooling during peak days.

- **Midweek Variations:** Thursday appears to have slightly lower congestion during the morning rush hour compared to other weekdays. This midweek relief from traffic stress can be advantageous for commuters.

- **Weekend Trends:** The chart indicates that congestion levels are significantly lower during the weekend, with Saturday and Sunday showing the lowest average congestion. This insight is beneficial for weekend travelers and those who prefer less congested routes.

- **Consistency on Weekdays:** The weekdays (Monday through Friday) exhibit relatively consistent congestion patterns. This consistency is crucial for city planners and commuters who rely on regular routes during the workweek.

- **Evening Rush Hour:** On weekday evenings, there is a notable uptick in congestion, particularly on Tuesdays and Wednesdays. Commuters planning their evening travel can use this information to consider alternative routes or transportation options.

- **Peak Congestion Hours:** For commuters who want to avoid the most congested times, the chart highlights that the morning rush hour between 7 AM and 9 AM, as well as the evening rush hour between 4 PM and 6 PM, are periods with the highest average congestion. 

In conclusion, the Weekly Average Congestion Line Chart simplifies complex data and offers valuable insights into weekly traffic patterns. Commuters can use this information to plan their trips strategically, and city planners can make data-driven decisions to improve traffic flow during peak hours.


### Visualization 3: Bar Chart of Top 10 Congested Arterial Streets

![bar](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/adf7ef53-c399-437e-9280-eaaaa51aff66)


The Bar Chart provides a straightforward and insightful representation of the top 10 congested arterial streets in the dataset. Each street is listed on the x-axis, while the y-axis indicates the average congestion levels (in terms of SPEED). The chart allows for a quick assessment of congestion issues on specific streets.

**Derived Insights:**

- **Highly Congested Streets:** The bar chart clearly identifies the top 10 arterial streets with the highest average congestion levels. These streets are the ones that typically experience the worst traffic conditions.

- **Congestion Variation:** By comparing the heights of the bars, it's evident that there are significant variations in congestion levels between different streets. This information is valuable for commuters who want to avoid highly congested routes.

- **Immediate Focus:** City planners and traffic engineers can use this visualization to pinpoint streets that require immediate attention for traffic management and optimization.

- **Data-Driven Decision Making:** This chart simplifies complex data, making it more accessible for decision-makers. By focusing on the most congested streets, authorities can allocate resources more effectively.

- **Color Palette:** The use of the 'viridis' color palette enhances the visual appeal and differentiation between streets, aiding in quick data interpretation.

In summary, the Bar Chart offers a concise and direct overview of the top congested arterial streets, enabling users to quickly identify streets with the most traffic issues and aiding decision-makers in addressing traffic congestion effectively.

### Visualization 4: Time Series Plot

![time](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/f4875aef-8594-4b4e-9a86-644c76897154)


The time series plot visualizes the number of buses (BUS_COUNT) on a Chicago street over the course of a day, with the hour of the day (HOUR) on the x-axis. The color of the lines represents different directions, indicating how many buses are present in each direction at various hours.

**Derived Insights:**

- **Rush Hour Patterns:** The time series plot reveals prominent peaks during typical rush hours. In the morning, around 7 AM, there is a notable increase in the number of buses, indicating high activity during the start of the workday. A similar pattern is observed in the late afternoon, around 4 PM, signifying the evening rush hour.

- **Directional Variation:** The color-coded lines for different directions provide insights into the directional distribution of buses. For example, in the morning peak, the blue line (indicating one direction) might be more pronounced than the orange line (indicating the opposite direction), suggesting a higher concentration of buses moving in that direction.

- **Midday Lulls:** During the mid-morning and early afternoon hours, there is a decrease in the number of buses, representing a period of lower activity. This aligns with the typical lull in transit activity between morning and evening rush hours.

- **Evening Rush Hour:** The increase in the number of buses during the late afternoon and early evening hours signifies the evening rush hour, with commuters returning home.

- **Consistent Patterns:** The time series plot shows consistent patterns on different days, helping users anticipate when buses are likely to be more crowded or when delays might occur.

- **Comparison of Directions:** Users can easily compare the number of buses in different directions, which can be useful for understanding traffic flow and planning routes.

In summary, the time series plot effectively visualizes how the number of buses changes throughout the day, allowing users to identify peak transit times and assess directional variations. This information can be valuable for commuters and city planners in optimizing public transportation services.


### Visualization 5: Hexbin Plot

![hexbin](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/e8a2ba49-4869-4c43-8ea0-ffe4035f9436)


The hexbin plot visualizes the relationship between two variables: bus count (x-axis) and congestion level (y-axis), with the size of hexagons representing segment length. This plot groups data points into hexagonal bins, allowing you to see the density of points and any patterns more clearly.

**Derived Insights:**

- **Density of Data Points:** The hexbin plot provides a clear view of data point density in different regions of the plot. Denser areas are represented by a higher concentration of smaller hexagons, while sparser areas have larger hexagons. 

- **Negative Relationship:** In the hexbin plot, there's a general trend indicating a negative relationship between bus count and congestion level. As the number of buses increases, the congestion level tends to decrease. This suggests that a higher number of buses can lead to smoother traffic flow.

- **Segment Length Impact:** The color of the hexagons represents segment length. Darker hexagons indicate longer segments. This additional dimension helps users understand how segment length relates to the bus count and congestion level.

- **Logarithmic Color Scale:** The use of a logarithmic color scale allows for better differentiation between segment lengths, emphasizing variations in longer segments while avoiding excessive color saturation in shorter segments.

- **Optimal Bus Count:** Users can identify regions with low congestion (towards the left of the plot) and high bus counts, indicating potentially optimal bus frequencies to maintain smooth traffic flow.

- **Sparse High Congestion:** Sparse, larger hexagons appear in the high congestion areas, indicating that, in regions with heavy congestion, longer segments are encountered less frequently.

- **Traffic Management Insights:** City planners and transportation authorities can use this plot to make data-driven decisions regarding bus scheduling, optimizing routes, and potentially reducing congestion by adjusting bus frequencies.

In summary, the hexbin plot effectively visualizes the relationship between bus count, congestion level, and segment length. It helps users identify patterns and density of data points, providing valuable insights into the impact of bus count on traffic congestion.

### Visualization 6: Bubble Chart of Bus Count, Congestion, and Segment Length

![bubble](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/cb9141fe-edeb-4d70-a0a8-3e267c61e1b4)


The bubble chart visualizes the relationships among three variables: bus count (x-axis), congestion level (y-axis), and segment length (bubble size). Each data point on the chart is represented by a bubble, and the size of the bubble corresponds to the segment length.

**Derived Insights:**

- **Bus Count vs. Congestion:** The chart shows that as the number of buses (bus count) increases (moving to the right on the x-axis), congestion level (congestion speed) tends to decrease. This suggests that a higher number of buses can lead to smoother traffic flow.

- **Congestion Spread:** There is a considerable spread in congestion levels for a similar bus count, indicating that other factors also influence traffic congestion.

- **Segment Length Impact:** Bubble sizes represent segment length, with larger bubbles indicating longer segments. This allows users to understand how segment length relates to bus count and congestion. Longer segments typically have a wider range of bus counts and congestion levels.

- **Color-Coded Segment Length:** Bubble colors are based on segment length, with the color intensity indicating longer or shorter segments. This provides an additional layer of information regarding segment characteristics.

- **Optimal Bus Count:** Users can identify regions with lower congestion and determine the corresponding bus count. This insight can be useful for optimizing bus schedules and routes.

- **Variability in Segment Length:** The chart reveals that segment length varies significantly. This information is valuable for understanding the distribution of road segments in terms of their lengths.

In summary, the bubble chart effectively visualizes the relationships between bus count, congestion, and segment length. It provides insights into how these factors interrelate and helps users understand the impact of bus count and segment length on congestion levels.

### Visualization 7: Box Plot of Monthly Congestion

![box](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/92a03756-f3fd-40a1-8b06-edcaf2146148)


The box plot visualizes the distribution of congestion levels (SPEED) for each month (MONTH). It consists of a series of box-and-whisker plots, one for each month, allowing us to identify variations in congestion throughout the year.

**Derived Insights:**

- **Monthly Congestion Distribution:** Each box plot represents a specific month, and it shows the distribution of congestion speeds within that month. The boxes represent the interquartile range (IQR), while the whiskers extend to the minimum and maximum values, excluding outliers.

- **Seasonal Patterns:** By examining the box plots, it is evident that different months exhibit varying congestion patterns. Some months have a wide spread of congestion levels, while others have congestion levels concentrated within a narrower range.

- **Outliers:** Outliers, represented as individual data points beyond the whiskers, are visible in some months. These outliers could indicate exceptional traffic conditions during specific months.

- **Monthly Comparisons:** The box plots allow users to compare congestion levels between months. For example, it's clear that certain months have consistently lower or higher congestion levels, which may be associated with seasonal factors like holidays or weather conditions.

- **Variability:** The variability in congestion levels between months is evident. This information is valuable for understanding the annual traffic patterns in the dataset.

In summary, the box plot of monthly congestion effectively reveals the distribution of congestion levels for each month, highlighting variations and seasonal patterns. Users can identify months with distinctive congestion patterns and better understand the influence of time of year on traffic conditions.

### Visualization 8: Seasonal Congestion Stacked Area Chart

![stack](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/6d8160b2-a159-423e-a8e2-1ee17a23da43)


The seasonal congestion stacked area chart visualizes how congestion levels (SPEED) vary over time (HOUR) throughout the year. Each month is represented by a different color in the stacked area chart, enabling the observation of seasonal patterns in traffic congestion.

**Derived Insights:**

- **Seasonal Patterns:** The stacked area chart reveals distinct seasonal patterns in congestion levels. Different months are represented by different colors, making it easy to identify variations in traffic congestion during different times of the year.

- **Monthly Comparisons:** By comparing the areas covered by each month's color, it's clear that some months consistently experience higher or lower congestion. This insight is valuable for understanding how seasonality affects traffic conditions.

- **Peak Congestion Hours:** Peak congestion hours can be identified by examining the highest points on the chart. The months in which these peak hours occur may vary, and this information can help travelers and city planners prepare for congestion during specific times of the day and year.

- **Interactions Between Months:** The stacked area chart also shows interactions between different months. For instance, during some hours, congestion levels may be higher in one month compared to others, indicating unique traffic patterns.

- **Visualization of Trends:** The chart offers a visually intuitive way to observe how congestion levels fluctuate over the course of a day and how these patterns change throughout the year.

In summary, the seasonal congestion stacked area chart effectively visualizes the seasonality of congestion levels by representing different months with distinct colors. It allows users to grasp seasonal patterns, identify peak congestion hours, and understand the interactions between months regarding traffic congestion.

### Visualization 9: Bar Chart of Top Congested Segments

![seg](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/d124989f-4888-44e5-a70e-9693acbd81ef)


The bar chart of top congested segments presents a list of traffic segments (SEGMENT_ID) with the highest average congestion levels (SPEED). This chart helps identify and rank the segments that experience consistent congestion.

**Derived Insights:**

- **Identification of Congested Segments:** The chart effectively highlights the top 10 traffic segments that consistently experience high levels of congestion. By listing the SEGMENT_ID values, it's easy to pinpoint which specific segments are affected.

- **Relative Congestion Levels:** The length of each horizontal bar represents the average congestion level (SPEED) for the respective segment. This allows for a quick visual comparison of congestion severity among the top congested segments.

- **Priority for Mitigation:** City planners, traffic engineers, and transportation authorities can use this chart to prioritize interventions and mitigation efforts in the segments with the most severe congestion.

- **Data-Driven Decision Making:** The chart provides valuable data to support data-driven decisions for managing and improving traffic flow in the identified segments.

- **Quick Reference:** The chart serves as a quick reference tool to identify the most problematic traffic segments, facilitating targeted actions for congestion relief.

In summary, the bar chart of top congested segments efficiently lists and ranks the segments with the highest average congestion levels. It provides a visual reference for identifying congested areas, enabling stakeholders to prioritize and implement solutions for these specific segments.

### Visualization 10: Scatter Plot

![scatter](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/144625177/d13a74fa-f973-424a-8abb-80fa613ee5c9)



The scatter plot displays the relationship between segment length (LENGTH) on the x-axis and congestion levels (SPEED) on the y-axis. Each data point represents a specific traffic segment, and the plot provides insights into how congestion levels are distributed across different segment lengths.

**Derived Insights:**

- **Distribution of Congestion Levels:** The scatter plot reveals the distribution of congestion levels within each range of segment lengths. By visualizing the data points, it's possible to identify patterns or trends in how congestion levels vary based on the length of the traffic segments.

- **Data Variability:** The spread of data points on the scatter plot indicates the variability of congestion levels for segments of different lengths. Clusters or patterns of points may suggest specific factors influencing congestion.

- **Segment Length Impact:** The plot allows for an analysis of whether segment length has a notable impact on congestion. It helps in understanding if shorter or longer segments tend to experience higher or lower congestion levels.

- **Outliers and Trends:** Outliers, if present, may indicate unique cases of extremely high or low congestion for specific segment lengths. The plot can also reveal any linear or non-linear trends in the data.

- **Decision Support:** This visualization can inform decisions related to urban planning, traffic management, and infrastructure development. For example, it may guide decisions on segment length optimization to reduce congestion.

In summary, the scatter plot effectively illustrates the relationship between segment length and congestion levels, offering insights into data distribution and variability. This visualization aids in understanding how congestion varies with segment length and provides valuable information for data-driven decision-making in traffic management and urban planning.

### Visualization 11: Grouped Bar Chart:

The implemented visualization is a grouped bar chart that compares the bus count (BUS_COUNT) and average speed (SPEED) for two different time periods: during the COVID-19 pandemic (2020-2021) and post-COVID (2022-2023).

 **Derived Insights:**

**During COVID-19 (2020-2021):**

![image](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/115042657/b01c52cb-c196-4921-b3e1-3d76e1877029)

- For most months during the COVID-19 period, there is a clear decrease in the bus count compared to the average speed. This suggests a reduction in the number of buses on the road during this time.
- The most significant drop in bus count relative to speed is observed in the 2nd and 8th months, but these values are not shown on the chart as they had negative speed values, which were excluded from the analysis.
- Despite the overall decrease in bus count, the average speed does not consistently increase; there is variation in speed levels across different months.

**Post-COVID (2022-2023):**

![image](https://github.com/uic-cs424/assignment-2-chicagobulls/assets/115042657/75c0a28b-7b09-4d58-a823-2b8271b47430)

- In the post-COVID period, the bus count and average speed show variations across different months.
- The 2nd and 8th months are included in this period, and the data suggests that there are still fluctuations in both bus count and average speed.
- While the general trend appears to be consistent with the earlier period (fewer buses correlate with higher speeds), there are likely other factors at play, as evident from the variations within each month.

  Overall, it can be observed that there is no major difference in bus count and their respective speeds during both periods.
