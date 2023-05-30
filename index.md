---
title: "📚 Project Title"
date: 20 March 2023
date-meta: 20 March 2023
---

# **Rank Student Accommodation Locations In London**

**Team members and collaboration:** 

- Qinzhi Liang -database maintenance
- Yan Su       -data collection
- Keyue Zhang  -data cleaning and transformation, data visulisation
- Ziqian Xiong -ducumentation

## 📝 **Introduction**


Our website is a valuable resource dedicated to assisting students in finding the ideal accommodation that perfectly suits their needs. We understand that choosing the right place to live is a significant decision, and we're here to make the process easier for you.

Through a comprehensive questionnaire survey, we have gathered insights from numerous students, enabling us to assign different weights to four important factors: crime rate, convenience, distance to pharmacies, transportation, and enjoyment. These weights have been determined based on the preferences and opinions of the student community, ensuring that our scoring system reflects their priorities.
![a photo of student accommodation](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/a%20photo%20of%20student%20dorm.jpeg)

### **Initial goals**

Our goal is to provide an objective and reliable assessment of each accommodation option, empowering students to make informed decisions. By incorporating the collective wisdom of fellow students, we offer a user-friendly platform that offers personalized recommendations and valuable information.

We understand that every student has unique preferences and requirements when it comes to choosing accommodation. Our website aims to simplify the selection process by providing a tailored experience. Whether you prioritize safety, convenience, access to healthcare, transportation, or overall enjoyment, our scoring system takes all these factors into account.

### **Motivations**

Motivated by the desire to enhance the accommodation selection process for students, our website provides a reliable resource that comprehensively assesses factors impacting the quality of student living. Discover a wealth of information to help you find the perfect accommodation that aligns with your unique preferences. Our platform supports you throughout this crucial decision-making process, enabling choices that enhance your overall student experience. With a data-driven approach and a commitment to student well-being, we aim to be your trusted companion in finding the ideal place to live during your educational journey. 

## 📊 **Data collection**

### **Data sources**

In order to achieve our goal on helping students to find student accommodations in London, with the factors influencing choosing student accommodation considered, we choose Google places APT, UK crime rates API and Four-square API as our data sources. Google maps API could help finding distance between accommodation and certain places (Universities, station etc.). gives us location of over 78 accommodations information of Chapter, Unite students, Urbanest, IQ and Scape. And the UK crime rate provide the crime rate data from 2019 to 2022 which helps accessing the safety level of certain accommodations. Moreover, the Foursquare API have the information of surrounding shops like supermarkets, pharmacies, pub etc., helping us evaluate the convenience level of accommodation.

### **Using API**

When using the Google map API, the latitude and longitude data of accommodations are collected, by pointing a place, then expanding the scope, we get the name of the site with the same keywords within and outside its scope. There is a sample of using google API.
![sample of using google API](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/data%20sample%20of%20using%20google%20map%20API.jpeg)

Using the crime rate API, there are different crime types including violent crime, weapon crime thefts and drugs. And in the Foursquare API, the diversity of surrounding shops is include which is a factor of assessing accommodations’ convenience level. 

## **Data cleaning**
### **Distance data cleaning problem**
Before getting all over these data scores combined, there are data cleaning problems worked out.

Initially, the method of calculating the distance was to match the address field of the obtained result with the latitude and longitude of the student dormitory. However, the results could not match actual situation. For example, when using this method to get a dormitory It takes 32 minutes to go to the supermarket, but if we try to search it with Google map, we find that it only takes one minute. 
![sample of data cleaning](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/Data%20cleaning%20of%20caculating%20distance.png)
To deal with it, we change the mode parameter in its API, which is changed from driving to walking by default. Also, to increase the accuracy of the destination, we separately changed the address from the result as the search word and changed it to use the place ID of Google map as the search. 

### **Crime rate and diversity data cleaning problem**

Moreover，
## **Scoring system**

We utilized two questionnaires to determine the weighting of different indicators in the ratings. Our first questionnaire consisted of five items: crime rate, rental prices, transport, accessibility, and diversity. Participants were asked to rank these five items in order of importance. A total of 55 volunteer participants completed the questionnaire. The results of this questionnaire provided us with a preliminary understanding of the weighting between the different options based on the collected data. However, due to the absence of a specific scale for evaluating the importance of the options and the limited number of participants, we questioned the scientific validity and objectivity of the questionnaire.

Consequently, we revised and improved the questionnaire. In our second questionnaire, we included an additional question regarding the gender and nationality of the participant. This was done to determine whether the participant belonged to our target sample, specifically international students in London. In order to address the lack of quantitative data, we implemented a rating scale. Participants were asked to rate the importance of each option on a scale from 0 to 100. By doing so, we obtained an average "importance score" for each item. The ratio of the mean scores for the different options was then calculated to determine the degree of influence of each indicator on the final rating.

However, it is important to note certain aspects of this questionnaire. Firstly, our options may not encompass all the thoughts and perspectives of the participants. Thus, the results may be biased if a participant selects an option that does not truly reflect their opinion. Additionally, since the participants complete the questionnaire in an uncontrolled environment, there may be extraneous variables that could affect the results. For instance, participants may experience reduced attention spans due to fatigue effect, which can potentially impact the outcomes. Nonetheless, as a self-report technique, the questionnaire provides a convenient means of understanding the participants' thoughts. Moreover, the use of quantitative data enables scientific calculations without any human bias.

Overall, these improvements aim to enhance the validity and reliability of the questionnaire in determining the weighting of indicators for the final ratings.

## 📈 **Data Analysis**
### **Rader diagrams analysis**

We used a radar chart (shown below) to show average and median scores of hostel brands across five factors, highlighting their strengths and weaknesses. This helps people choose the right hostel. However, it's important to remember that this chart only represents each hostel's traits and cannot be used to compare different accommodation brands. This limitation comes from using average and median values due to the varying number of halls of residence among brands.
#### **IQ Apartments**
![iQ mean radar](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/iq%20mean%20radar%20graph.jpeg) 
![iq median radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/iq%20median%20radar%20diagram.png)

IQ Apartments has some notable advantages based on the radar chart. The “transportation” and “pharmacy" factor stands out with a high score of 4, indicating excellent access to different transportation options, which is highly convenient. Additionally, both "food & dairy products"received scores about 3.6, suggesting decent nearby options for essential goods and services.

However, there are a couple of potential disadvantages. The scores of 3 for both "safety score" and "diversity of surrounding shops" while the safety score is not particularly low, there may be some aspects that need attention. Similarly, the score for the diversity of surrounding shops implies limited options nearby.

The median score for IQ flat is similar to the average for all factors, showing consistent overall performance. However, the slightly higher score in 'food and dairy' suggests better availability or quality of food and dairy products nearby.

Therefore, IQ Apartments offer advantages like convenient transportation and access to essential goods and services. However, potential disadvantages include safety measures and limited diversity in nearby shops.


#### **Unite students apartments**

Based on the radar charts(shown below), Unite Students Apartments have both advantages and potential disadvantages. It excels in "transportation" and "pharmacy" with a score of 4, indicating excellent access to transportation and pharmacy services, which is highly convenient for residents.
![unite students mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/Unite%20students%20mean%20radar%20diagram.png)
![unite students median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/Unite%20students%20median%20radar%20graph.png)
In terms of convenience, it also scores reasonably well with 3.3 for "diversity of surrounding shops" and 3.4 for "food & dairy products," suggesting a decent variety of shops and food options nearby.

However, there are a couple of potential disadvantages. The "safety score" has an average of 2.8, indicating room for improvement in safety measures. Additionally, the median score of 2.6 for "safety score" suggests inconsistency or differing perceptions of safety among residents.

To summarize, Unite Students Apartments offer advantages in transportation, access to essential services, and nearby shops and food options. However, there may also be potential disadvantages related to safety that should not be overlooked when choosing accomadation.

#### **Urbanest**

For urbanest's accommodations, based on the radar charts shown below, The scores of 3.4 for "safety score" might appears that Urbanest Apartments might have a potential disadvantage in terms of safety, as indicated by the relatively lower score. It suggests that there may be areas for improvement in ensuring a safer environment within the apartment complex or its surroundings.
![urbanest mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/urbanest%20mean%20radar%20diagram.png)
![urbanest median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/urbanest%20median%20radar%20diagram.png)

Also, the score of 2.9 for "diversity of surrounding shops" indicates that there might be limitations in terms of the variety or range of shops available in the vicinity. This could impact residents' choices and convenience when it comes to shopping options.

However, it's important to note that Urbanest Apartments still have notable advantages, such as excellent transportation options, convenient access to pharmacy services, and a good variety of food and dairy products. Despite the lower safety score, the other factors seem to be rated highly, which can contribute to the overall appeal of the apartment.

When considering the median score, which is broadly similar to the average across all factors, there is still an obvious decrease specifically in the 'pharmacy' option. This suggests some potential inconsistency or lower perceptions regarding pharmacy availability or quality among residents.

To conclude, while Urbanest Apartments offer advantages such as transportation convenience,and access to pharmacy services, there may be a potential disadvantage in terms of safety and shopping options, as indicated by the lower score. 

#### **Chapter Apartments**
Based on the radar chars shown below, Chapter Apartments have strengths and one possible weakness. Advantages include high scores of 4 for "transportation" and "pharmacy," indicating excellent transportation options and convenient access to pharmacies. Scores of 3.5 for "food & dairy products" suggest a satisfactory food options.

![Chapter mean radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/chapter%20mean%20radar%20diagram.png)
![Chapter median radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/chapter%20median%20diagram.png)

However, Chapter Apartments might have a potential disadvantage in terms of safety, as indicated by the relatively lower score of 3. It suggests that there may be areas for improvement in ensuring a safer environment within the apartment complex or its surroundings.

The median score is similar to the average overall, but notably lower for "diversity of surrounding shops." This suggests some variability or lower perceptions of shop diversity among residents. 

Overall, while Chapter Apartments offer advantages such as transportation convenience, access to pharmacy services, and a satisfactory range of food options, there may be a potential disadvantage in terms of safety, as indicated by the lower score.



#### **Scape Apartments**
Based on the radar charts shown below, Scape Apartments have both advantages and potential disadvantages. They excel in "pharmacy" with a high score of 4, providing excellent access to essential services. They also have reasonable safety measures (3.6), a satisfactory variety of nearby shops (3.3), and decent options for food and dairy products (3.7).
![Scape mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/scape%20mean%20radar%20diagram.png)
![Scape median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/scape%20median%20radar%20diagram.png)
However, a potential drawback is the score of 3 for "transportation," indicating room for improvement in available transportation options near the complex. The median score, similar to the average, shows an increase in the 'diversity of surrounding shops,' suggesting a higher variety of nearby shops, which is advantageous for residents.

In summary, Scape Apartments offer convenient access to pharmacies, reasonable safety measures, satisfactory nearby shops, and food options. However, transportation options may need improvement.
### **Boxplot patterns analysis**
#### **Crime rate analysis**
![crimte rate boxplot graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/crime%20rate%20score%20boxplot%20graph.jpeg)

In the boxplot diagram of crime rate scores of each brand, Urbanest’s accommodations have the highest median which means higher safety level, compared with the lowest median of the Unite students. Therefore, the accommodations of Unite students are not really competitive in safety aspect. Also, Scape and Scape provide similar quality of safety level of accommodations.
#### **Average time to food service analysis**
![averge time to nearby food service](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/avg%20time%20to%20food%20service%20boxplot%20graph.jpeg)
In the food service aspect, Urbanest’ accommodations have lower median, indicating easier access to supermarkets, convenience and restaurants. While Unite students has the highest median which means students staying here have to spend more time in hunting food.

#### **Averge time to nearby phamarmacy analysis**
![averge time to nearby phamarmacy](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/avg%20time%20to%20nearby%20pharmacy%20boxplot%20graph.jpeg)
In the aspect of accessing to pharmacy, Chapter with lowest median gives lowest median, indicating shortest time to get to nearby pharmacy. Although Urbanest has greater median, their difference are not extremely significant. However, the outlier of IQ, which has a greatly long time in accessing to pharmacy should not be ignored

#### **Average time to subway and bus stops**
![avg time to subway and bus stations boxplot graoh](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/4a6e3af28d9e38ebfca72d97a34664eff1e27eec/figures/avg%20time%20to%20subway%20and%20bus%20stations%20boxplot%20graph.jpeg)
Based on the data provided, it is possible to compare the average time taken to reach a bus or metro stop for different hostel brands. The 'iQ' and 'Urbanest' brands have relatively low median and interquartile values, indicating a shorter average travel time. However, it is worth noting that both brands have outliers, indicating occasional unusually long travel times. On the other hand, the 'Unite students' and 'Chapter' brands exhibit higher median and interquartile values, indicating longer average travel times, but without any significant outliers. In contrast, the 'Scape' brand stood out with a longer average travel time, and it did have an outlier. This suggests that, in most cases, this brand has a longer average travel time, but occasionally there are instances where the travel time is significantly longer. Based on these analyses, the 'iQ' and 'Urbanest' may be more convenient for commuting as they have shorter average travel times, despite the outliers.
#### **Diversity of surrounding shops**
![num of different stores around boxplot graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/06cb09680d1b83904ec6cf9565eac7fd9b12acbd/figures/num%20of%20different%20stores%20around%20boxplot%20graph.png)

The 'Scape' brand has the highest median (55), indicating a potentially higher number of surrounding shops compared to the slightly lower median of the 'Unite students' brand, with other brands falling in between. This suggests that 'Scape' may offer a greater variety of shops nearby. In terms of dispersion, 'Scape' has a concentrated upper quartile, while 'Unite students' has a relatively lower upper quartile, indicating that 'Scape' data is more concentrated in higher values. Regarding outliers, 'iq' has four, 'Unite students' has two, and 'Scape' has one outlier, while 'Urbanest' and 'Chapter' have none. Thus, 'Urbanest' and 'Chapter' are relatively stable, while 'Scape' performs well in terms of surrounding shops, data concentration, and stability compared to 'iq' and 'Unite students'.




## 🖼️ **Results**
![top 10 dorm ranking](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/3007ba2a202394fe664f8280a34bf4bd1968b245/figures/top%2010%20dorm%20ranking.jpg)

We have finally selected the ten highest scoring student residences based on our scoring system (As shown in the chart). Unite students made up the highest percentage of the top ten, followed by urbanest, iQ and Chapter. none of the flats in Scape made it into the top ten. Students can refer to this ranking when choosing their accommodation and select the accommodation that meets their expectations.

![pie chart](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/fec01a11c50ba3f44179bd1bfa0fb84d33c4537a/figures/pie%20chart.png)

#### **Conclusion**
To assist international students in London in selecting suitable accommodation, we have developed a rating system. This system evaluates common student accommodations and provides a meaningful ranking. We employed a questionnaire to gather quantitative data, aiming to understand the overall perception of London students regarding the importance of various factors. The final ranking was determined by considering indicators such as "safety," "diversity of surrounding shops," "transportation," "food and dairy products," and "pharmacy." The weighting of these factors in the final score was determined based on their perceived importance as indicated by the questionnaire participants. We utilized box plots and radar plots to not only compare and contrast the strengths and weaknesses of each factor across different hostel brands but also to identify the overall strengths and weaknesses of each individual hostel brand. As a result, we identified the ten highest-scoring student residences, providing students with the opportunity to choose the most suitable residence for their needs.

## 📚 **Reference Links**
1. [Google Maps](https://www.google.co.uk/maps).
2. [IQ Student Accommodation](https://www.iqstudentaccommodation.com/).
3. [Unite Student Accommodation](https://www.unitestudents.com/london).
4. [Urbanest Accommodation](https://uk.urbanest.com/).
5. [Chapter Accommodation ](https://www.chapter-living.com/).
6. [Scape Accommodation](https://www.scape.com/).
