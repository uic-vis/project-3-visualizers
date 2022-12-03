**CS 424 - Visualization and Visual Analytics - Project 3**

**Abstract:**

Traffic crashes have been the main reason for the increase in deaths. There can be many factors that contribute to these crashes like road maintenance, driver behavior, weather, speed limits, etc. As part of our study, we examined the impact of traffic crashes during nighttime versus daytime and their effect on particular attributes (Gender, age, county, and airbag deployment).

**Data Set Description:**

Each data row represents information about a traffic crash that occurred in Chicago. We have used a subset of our dataset that covers the last 1 year of data on the crashes. We did so since our dataset is too large to fit into Observable. For Final Visualization, we used Traffic - Crashes data.

**Initial Questions: (Recap)**

**Domain Question: What effect does the time of day have on crashes?**

Despite our best efforts to avoid driving at night, our research shows that no matter what time of day it is, the number of accidents is close to the same whether it is day or night. In order to limit these losses as much as possible, we believe it is important to take a stand on accident prevention.

**Q1: What is the correlation between age and the time (day/night) of a crash?**

**Q2: What effect does the time of the day have on the gender involved in a crash?**

**Q3: What effect does the time of the day have on crashes in every county?**

**Data Transformation:**

We used a subset of the dataset since our dataset is large. We see fit to use the last 1 year records of the data to reduce the size and fit it into observable. Using Pandas, we pre-processed the data to remove the NULL/NAN values and also sliced the data for only important attributes. We performed data transformation for spatial analysis and temporal analysis. The major attributes in our dataset are Timestamp, Age, Sex, and Zipcodes. Later on, we have also used Airbag Deployment as one of the major attributes for our visualizations.

**Encodings / Interactions:**

**Q1: What is the correlation between age and the time (day/night) of a crash?**

` `**![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.001.png)**

**Fig 1: Bar Graph where the X axis represents the day of the hour and the Y axis represents the average age of people involved in a crash**

**Observation:** The bar graph shows that the average age of the person involved in a crash increases as the day progresses and decreases at night. Therefore, young drivers are more involved in night crashes and older people are more involved in daytime crashes.

**Q2: What effect does the time of the day have on the gender involved in a crash?**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.002.png)

**Fig 2: Line graph where X axis represents the number of crashes and Y axis represents the hour of the day. It shows the total number of crashes.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.003.png)

**Fig 3: Represents the number of crashes where only the drivers were involved.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.004.png)

**Fig 4: Represents the number of crashes where only the passengers were involved.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.005.png)

**Fig 5: Our visualization has a drop-down list that lets us select the type of person involved in the crash.**

**Observation :** Though the line graph shows us that the number of males involved in crashes is more than females, the trend of both men and women is similar in all 3 cases. Therefore, we can say there is not much effect of the time of the crash on gender.

**Q3: What effect does the time of the day have on crashes in every county?**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.006.png)

**Fig 6: Choropleth map representing the number of crashes during the day and night over the span of one year for every county in Chicago.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.007.png)

**Fig 7: Hovering over a county shifts the focus onto it, the rest get blurred.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.008.png)

**Fig 8:  Selecting a county, the number of male, female crashes, age distribution, and zip code of that county are displayed.**

**Observation:** The information retrieved from the Choropleth map shows us that few of the counties have more accidents in daylight conditions than at night. Counties - 60623 and 60629 have an equally high number of crashes during the day and night. This may be due to more traffic, road conditions, and population. etc



**New Visualizations**

**Multi View**

**Q4: What is the relationship between Air bag deployed classification and month of the year, along with gender?**

Here, we used a stacked bar chart to represent the action of the airbag deployment in crashes throughout every month. We can see that all the different categories (airbag classification) are consistent except for in a few cases. We have also added interactivity that lets us click on a section, which shows the number of crashes related to a gender, which is consistent among all the sections. Therefore, we can conclude that gender does not have any effect on air bag deployment and also month of year has minimal effect on air bag deployment.

The attributes we have used in this visualization are number of crashes, month, and airbag deployed.

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.009.png)

**Fig 9: Clicking on the subsections of the stacked bar chart shows the number of male and female crashes along with the section that has been selected.**


![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.010.png)

**Fig 10: Number of male and female crashes upon clicking the stacked bar.**

**Spatial View**
## **Spatial visualization of crashes in Chicago in March, 2020.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.011.png)

**Fig 11: OpenStreetMap shows the number of crashes across the regions of Chicago.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.012.png)

**Fig 12: Zoomed in version of the map. Shows a crash with the area and number of the month upon clicking a location.**

![](img/Aspose.Words.f7598c5b-c390-4828-b4a1-a8743c4862aa.013.png)

**Fig 13: Selecting the marker updates the value in the Age vs Hour map.**

For the spatial view, we took data from March 2020 to reduce the data. We observe that during the peak of lock down, we see a  significant number of crashes across all the regions of chicago but the number of crashes are almost double in the south side of chicago than in the loop and very low in the outskirts of Chicago.

As we hover over the regions on the map, we can see a blue outline around that region and a coloured circle that shows the number of crashes that occurred. We can zoom in to check the number of crashes in every street. There is a speech bubble that pops up showing us the area and the hour of the day the crash occurs.

For interactivity, By zooming on the map, Select a marker which is the location of the marker and the hour of the accident gets updates in the (Age vs Hour of the Day)bar graph shown in the first page. The bar graph gets updated at the end of the page.


**Initial Findings:**

We have analyzed data with respect to Gender, age and county with the time of the day. Our analysis is as shown above. We have also added two new visualizations that show the correlation between airbag deployment classification and the crashes and also an OpenStreetMap that represents crashes across all the regions of Chicago.

Here is a link to our visualization solution: https://vivekkvn.github.io/CS424_Final/

**Conclusion/Insights:**

According to our study, young aged drivers are more involved in crashes that occur at night than older aged people. Due to the similar trend in both genders, we can say that the time of day does not affect the number of crashes of a particular gender. As for the counties in Chicago, a few of the neighborhoods have relatively higher crashes during the day than at night. According to our two new visualizations, gender doesn’t have any effect on the airbag deployment and so does the month of the year. It also shows that the crash rate is almost double of the crash rate in the loop and in the outskirts , it is relatively less during March 2020.
