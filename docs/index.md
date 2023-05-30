---
title: "📚 Project Title"
date: 20 March 2023
date-meta: 20 March 2023
---

# Rank Student Accommodation Locations In London

**Team members:** 

- Qinzhi Liang
- Yan Su
- Keyue Zhang
- Ziqian Xiong

## 📝 Project Description

**Introduction**

Our website is a valuable resource dedicated to assisting students in finding the ideal accommodation that perfectly suits their needs. We understand that choosing the right place to live is a significant decision, and we're here to make the process easier for you.

Through a comprehensive questionnaire survey, we have gathered insights from numerous students, enabling us to assign different weights to four important factors: crime rate, convenience, distance to pharmacies, transportation, and enjoyment. These weights have been determined based on the preferences and opinions of the student community, ensuring that our scoring system reflects their priorities.

**Initial goals**

Our goal is to provide an objective and reliable assessment of each accommodation option, empowering students to make informed decisions. By incorporating the collective wisdom of fellow students, we offer a user-friendly platform that offers personalized recommendations and valuable information.

We understand that every student has unique preferences and requirements when it comes to choosing accommodation. Our website aims to simplify the selection process by providing a tailored experience. Whether you prioritize safety, convenience, access to healthcare, transportation, or overall enjoyment, our scoring system takes all these factors into account.
Motivations

Motivated by the desire to enhance the accommodation selection process for students, our website provides a reliable resource that comprehensively assesses factors impacting the quality of student living. Discover a wealth of information to help you find the perfect accommodation that aligns with your unique preferences. Our platform supports you throughout this crucial decision-making process, enabling choices that enhance your overall student experience. With a data-driven approach and a commitment to student well-being, we aim to be your trusted companion in finding the ideal place to live during your educational journey. 

## 📊 Data

**Data sources**

In order to achieve our goal on helping students to find student accommodations in London, with the factors influencing choosing student accommodation considered, we choose Google places APT, UK crime rates API and Four-square API as our data sources. Google maps API could help finding distance between accommodation and certain places (Universities, station etc.). gives us location of over 78 accommodations information of Chapter, Unite students, Urbanest, IQ and Scape. And the UK crime rate provide the crime rate data from 2019 to 2022 which helps accessing the safety level of certain accommodations. Moreover, the Foursquare API have the information of surrounding shops like supermarkets, pharmacies, pub etc., helping us evaluate the convenience level of accommodation.

**Using API**

When using the Google map API, the latitude and longitude data of accommodations are collected, by pointing a place, then expanding the scope, we get the name of the site with the same keywords within and outside its scope. Using the crime rate API, there are different crime types including violent crime, weapon crime thefts and drugs. And in the Foursquare API, the diversity of surrounding shops is include which is a factor of assessing accommodations’ convenience level. (Picture needed) 

**Data cleaning**

Before getting all over these data scores combined, there are data cleaning problems worked out.

Initially, the method of calculating the distance was to match the address field of the obtained result with the latitude and longitude of the student dormitory. However, the results could not match actual situation. For example, when using this method to get a dormitory It takes 32 minutes to go to the supermarket, but if we try to search it with Google map, we find that it only takes one minute. To deal with it, we change the mode parameter in its API, which is changed from driving to walking by default. Also, to increase the accuracy of the destination, we separately changed the address from the result as the search word and changed it to use the place ID of Google map as the search. (Picture needed) 

**Scoring system**

We utilized two questionnaires to determine the weighting of different indicators in the ratings. Our first questionnaire consisted of five items: crime rate, rental prices, transport, accessibility, and diversity. Participants were asked to rank these five items in order of importance. A total of 55 volunteer participants completed the questionnaire. The results of this questionnaire provided us with a preliminary understanding of the weighting between the different options based on the collected data. However, due to the absence of a specific scale for evaluating the importance of the options and the limited number of participants, we questioned the scientific validity and objectivity of the questionnaire.

Consequently, we revised and improved the questionnaire. In our second questionnaire, we included an additional question regarding the gender and nationality of the participant. This was done to determine whether the participant belonged to our target sample, specifically international students in London. In order to address the lack of quantitative data, we implemented a rating scale. Participants were asked to rate the importance of each option on a scale from 0 to 100. By doing so, we obtained an average "importance score" for each item. The ratio of the mean scores for the different options was then calculated to determine the degree of influence of each indicator on the final rating.

However, it is important to note certain aspects of this questionnaire. Firstly, our options may not encompass all the thoughts and perspectives of the participants. Thus, the results may be biased if a participant selects an option that does not truly reflect their opinion. Additionally, since the participants complete the questionnaire in an uncontrolled environment, there may be extraneous variables that could affect the results. For instance, participants may experience reduced attention spans due to fatigue effect, which can potentially impact the outcomes. Nonetheless, as a self-report technique, the questionnaire provides a convenient means of understanding the participants' thoughts. Moreover, the use of quantitative data enables scientific calculations without any human bias.

Overall, these improvements aim to enhance the validity and reliability of the questionnaire in determining the weighting of indicators for the final ratings.

## 📈 Analysis
![picture of top 10 ranking of students accomodation](https://github.com/Judy-45/LSE-DS105-Data-Dwelling-Detectives/blob/main/Data%20cleaning%20of%20caculating%20distance.png)


## 🖼️ Results

## 🖋️ Conclusions

## 📚 References
