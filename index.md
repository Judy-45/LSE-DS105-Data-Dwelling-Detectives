---
title: "📚 Project Title"
date: 20 March 2023
date-meta: 20 March 2023
---

# **Rank Student Accommodation Locations In London**

**Team members:** 

- Qinzhi Liang
- Yan Su
- Keyue Zhang
- Ziqian Xiong

## 📝 **Introduction**



Our website is a valuable resource dedicated to assisting students in finding the ideal accommodation that perfectly suits their needs. We understand that choosing the right place to live is a significant decision, and we're here to make the process easier for you.

Through a comprehensive questionnaire survey, we have gathered insights from numerous students, enabling us to assign different weights to four important factors: crime rate, convenience, distance to pharmacies, transportation, and enjoyment. These weights have been determined based on the preferences and opinions of the student community, ensuring that our scoring system reflects their priorities.

### **Initial goals**

Our goal is to provide an objective and reliable assessment of each accommodation option, empowering students to make informed decisions. By incorporating the collective wisdom of fellow students, we offer a user-friendly platform that offers personalized recommendations and valuable information.

We understand that every student has unique preferences and requirements when it comes to choosing accommodation. Our website aims to simplify the selection process by providing a tailored experience. Whether you prioritize safety, convenience, access to healthcare, transportation, or overall enjoyment, our scoring system takes all these factors into account.

### **Motivations**

Motivated by the desire to enhance the accommodation selection process for students, our website provides a reliable resource that comprehensively assesses factors impacting the quality of student living. Discover a wealth of information to help you find the perfect accommodation that aligns with your unique preferences. Our platform supports you throughout this crucial decision-making process, enabling choices that enhance your overall student experience. With a data-driven approach and a commitment to student well-being, we aim to be your trusted companion in finding the ideal place to live during your educational journey. 

## 📊 **Data collection**

### **Data sources**

In order to achieve our goal on helping students to find student accommodations in London, with the factors influencing choosing student accommodation considered, we choose Google places APT, UK crime rates API and Four-square API as our data sources. Google maps API could help finding distance between accommodation and certain places (Universities, station etc.). gives us location of over 78 accommodations information of Chapter, Unite students, Urbanest, IQ and Scape. And the UK crime rate provide the crime rate data from 2019 to 2022 which helps accessing the safety level of certain accommodations. Moreover, the Foursquare API have the information of surrounding shops like supermarkets, pharmacies, pub etc., helping us evaluate the convenience level of accommodation.

### **Using API**

When using the Google map API, the latitude and longitude data of accommodations are collected, by pointing a place, then expanding the scope, we get the name of the site with the same keywords within and outside its scope. Using the crime rate API, there are different crime types including violent crime, weapon crime thefts and drugs. And in the Foursquare API, the diversity of surrounding shops is include which is a factor of assessing accommodations’ convenience level. (Picture needed) 

## **Data cleaning**

Before getting all over these data scores combined, there are data cleaning problems worked out.

Initially, the method of calculating the distance was to match the address field of the obtained result with the latitude and longitude of the student dormitory. However, the results could not match actual situation. For example, when using this method to get a dormitory It takes 32 minutes to go to the supermarket, but if we try to search it with Google map, we find that it only takes one minute. To deal with it, we change the mode parameter in its API, which is changed from driving to walking by default. Also, to increase the accuracy of the destination, we separately changed the address from the result as the search word and changed it to use the place ID of Google map as the search. (Picture needed) 

## **Scoring system**

We utilized two questionnaires to determine the weighting of different indicators in the ratings. Our first questionnaire consisted of five items: crime rate, rental prices, transport, accessibility, and diversity. Participants were asked to rank these five items in order of importance. A total of 55 volunteer participants completed the questionnaire. The results of this questionnaire provided us with a preliminary understanding of the weighting between the different options based on the collected data. However, due to the absence of a specific scale for evaluating the importance of the options and the limited number of participants, we questioned the scientific validity and objectivity of the questionnaire.

Consequently, we revised and improved the questionnaire. In our second questionnaire, we included an additional question regarding the gender and nationality of the participant. This was done to determine whether the participant belonged to our target sample, specifically international students in London. In order to address the lack of quantitative data, we implemented a rating scale. Participants were asked to rate the importance of each option on a scale from 0 to 100. By doing so, we obtained an average "importance score" for each item. The ratio of the mean scores for the different options was then calculated to determine the degree of influence of each indicator on the final rating.

However, it is important to note certain aspects of this questionnaire. Firstly, our options may not encompass all the thoughts and perspectives of the participants. Thus, the results may be biased if a participant selects an option that does not truly reflect their opinion. Additionally, since the participants complete the questionnaire in an uncontrolled environment, there may be extraneous variables that could affect the results. For instance, participants may experience reduced attention spans due to fatigue effect, which can potentially impact the outcomes. Nonetheless, as a self-report technique, the questionnaire provides a convenient means of understanding the participants' thoughts. Moreover, the use of quantitative data enables scientific calculations without any human bias.

Overall, these improvements aim to enhance the validity and reliability of the questionnaire in determining the weighting of indicators for the final ratings.

## 📈 **Data Analysis**

We have utilized a radar chart to depict the average and median scores of each hostel brand across the five factors, aiming to showcase the strengths and weaknesses of different hostel brands and assist potential residents in selecting the most suitable hostel for their needs. It is important to note that this chart solely reflects the characteristics of each individual hostel and is not suitable for comparing different accomadation brands. This limitation arises from the utilization of average and median figures, as the number of halls of residence significantly varies across brands.

![iq mean radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/IQ%20mean%20radar%20diagram.png) 
![iq median radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/iq%20median%20radar%20diagram.png)

IQ Apartments has some notable advantages based on the radar chart. The “transportation” and “pharmacy" factor stands out with a high score of 4, indicating excellent access to different transportation options, which is highly convenient. Additionally, both "food & dairy products"received scores about 3.6, suggesting decent nearby options for essential goods and services.

However, there are a couple of potential disadvantages. The scores of 3 for both "safety score" and "diversity of surrounding shops" while the safety score is not particularly low, there may be some aspects that need attention. Similarly, the score for the diversity of surrounding shops implies limited options nearby.

The median score for IQ flat is similar to the average for all factors, showing consistent overall performance. However, the slightly higher score in 'food and dairy' suggests better availability or quality of food and dairy products nearby.

In summary, IQ Apartments offer advantages like convenient transportation and access to essential goods and services. However, potential disadvantages include safety measures and limited diversity in nearby shops.


Unite students

Based on the radar chart, Unite Students Apartments have both advantages and potential disadvantages. It excels in "transportation" and "pharmacy" with a score of 4, indicating excellent access to transportation and pharmacy services, which is highly convenient for residents.
![unite students mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/Unite%20students%20mean%20radar%20diagram.png)
![unite students median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/Unite%20students%20median%20radar%20graph.png)
In terms of convenience, it also scores reasonably well with 3.3 for "diversity of surrounding shops" and 3.4 for "food & dairy products," suggesting a decent variety of shops and food options nearby.

However, there are a couple of potential disadvantages. The "safety score" has an average of 2.8, indicating room for improvement in safety measures. Additionally, the median score of 2.6 for "safety score" suggests inconsistency or differing perceptions of safety among residents.

To summarize, Unite Students Apartments offer advantages in transportation, access to essential services, and nearby shops and food options. However, there may also be potential disadvantages related to safety that should not be overlooked when choosing accomadation.

Urbanest

For urbanest's accommodations, based on the radar chart, The scores of 3.4 for "safety score" might appears that Urbanest Apartments might have a potential disadvantage in terms of safety, as indicated by the relatively lower score. It suggests that there may be areas for improvement in ensuring a safer environment within the apartment complex or its surroundings.
![urbanest mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/urbanest%20mean%20radar%20diagram.png)
![urbanest median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/urbanest%20median%20radar%20diagram.png)

Also, the score of 2.9 for "diversity of surrounding shops" indicates that there might be limitations in terms of the variety or range of shops available in the vicinity. This could impact residents' choices and convenience when it comes to shopping options.

However, it's important to note that Urbanest Apartments still have notable advantages, such as excellent transportation options, convenient access to pharmacy services, and a good variety of food and dairy products. Despite the lower safety score, the other factors seem to be rated highly, which can contribute to the overall appeal of the apartment.

When considering the median score, which is broadly similar to the average across all factors, there is still an obvious decrease specifically in the 'pharmacy' option. This suggests some potential inconsistency or lower perceptions regarding pharmacy availability or quality among residents.

In summary, while Urbanest Apartments offer advantages such as transportation convenience,and access to pharmacy services, there may be a potential disadvantage in terms of safety and shopping options, as indicated by the lower score. 

Chapter
Based on the radar chart, Chapter Apartments have strengths and one possible weakness. Advantages include high scores of 4 for "transportation" and "pharmacy," indicating excellent transportation options and convenient access to pharmacies. Scores of 3.5 for "food & dairy products" suggest a satisfactory food options.

![Chapter mean radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/chapter%20mean%20radar%20diagram.png)
![Chapter median radar diagram](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/chapter%20median%20diagram.png))

However, Chapter Apartments might have a potential disadvantage in terms of safety, as indicated by the relatively lower score of 3. It suggests that there may be areas for improvement in ensuring a safer environment within the apartment complex or its surroundings.

The median score is similar to the average overall, but notably lower for "diversity of surrounding shops." This suggests some variability or lower perceptions of shop diversity among residents. 

In summary, while Chapter Apartments offer advantages such as transportation convenience, access to pharmacy services, and a satisfactory range of food options, there may be a potential disadvantage in terms of safety, as indicated by the lower score.



Scape
Based on the radar chart, Scape Apartments have both advantages and potential disadvantages. They excel in "pharmacy" with a high score of 4, providing excellent access to essential services. They also have reasonable safety measures (3.6), a satisfactory variety of nearby shops (3.3), and decent options for food and dairy products (3.7).
![Scape mean radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/scape%20mean%20radar%20diagram.png)
![Scape median radar graph](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/figures/scape%20median%20radar%20diagram.png)
However, a potential drawback is the score of 3 for "transportation," indicating room for improvement in available transportation options near the complex. The median score, similar to the average, shows an increase in the 'diversity of surrounding shops,' suggesting a higher variety of nearby shops, which is advantageous for residents.

To summarize, Scape Apartments offer convenient access to pharmacies, reasonable safety measures, satisfactory nearby shops, and food options. However, transportation options may need improvement.




### **crime rate**
### **most convenient accomodation locations**
#### **y-axis: mins**
### **correlation between rent price**
#### **heatmap**
#### **line chart**
![picture of top 10 ranking of students accomodation](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/Data%20cleaning%20of%20caculating%20distance.png)


## 🖼️ **Results**
### **top 5 according to scoring system**
### **last 5 according to scoring system**




## 📚 **References**
