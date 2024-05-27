![image](https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/7e3dc7ec-f1d5-4f8f-9b72-a846c2d7af1c)# Accenture SocialBuzz Job Simulation

## Overview

Welcome to the Accenture SocialBuzz Job Simulation! This README will guide you through the data sets provided, the data model, and the steps to analyze the data to answer specific business questions.

## Client Details

Social Buzz, founded by ex-engineers from a major social media company, emphasizes content over user identity. With 500 million monthly users, it faces challenges managing vast unstructured data and seeks advisory help for scaling and preparing for an IPO. Despite a technical team of 200, the company lacks resources to manage its rapid growth and desires to learn data best practices from external experts. Until this point, they have not relied on any third party firms to help them get to where they are. However there are 3 main reasons why they are now looking at bringing in external expertise:

     1) They are looking to complete an IPO by the end of next year and need guidance to ensure that this goes smoothly.
     
     2) They are still a small company and do not have the resources to manage the scale that they are currently at. They could hire more people, but they want an experienced practice to help instead.
     
     3) They want to learn data best practices from a large corporation. Due to the nature of their business, they have a massive amount of data so they are keen.

#### Aim as a Data Analyst : Analysis to find Social Buzz’s top 5 popular categories of content.

### Data Sets

There are 3 data sets provided, each containing different columns and values. These data sets are crucial for understanding social media trends and interactions. They include:

1. **Reaction**: Contains data on user reactions to various social media content.
2. **Content**: Provides information about the social media content itself.
3. **Reaction Types**: Defines different types of reactions users can have.

### Data Model

The data model illustrates the relationships between all data sets and any links that can be used to merge tables. Understanding this model is essential for effectively analyzing the data.

 <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/6ff99910-aa97-4fd6-b7c2-77cac457bb88" alt="Image Description" width="500">

### Steps for Analysis

To ensure you're using the correct data to answer business questions, follow these steps:

1. **Requirements Gathering**
2. **Data Cleaning**
3. **Data Modelling**
4. **Data Analysis**
5. **Data Visualization**
6. **Presentation in the form of storytelling**

### Business Question

The primary business question for this simulation is to determine the top 5 categories with the largest popularity on social media.

## Steps to Answer the Business Question

1. **Create a Final Data Set**

   Merge the relevant data sets together to form a final comprehensive data set. 
2. **Figure Out the Top 5 Performing Categories**

   Calculate the total scores for each category by summing up the relevant metrics. You can utilize formulas like "Sum If" to efficiently perform this calculation.

For a detailed presentation and storytelling video, please access the following resources:

## Presentation and Storytelling

- **PowerBI Link**: [Accenture SocialBuzz PowerBI Dashboard][Presentation File](path/to/Data%20Analytics%20template%20-%20Task%203_final%20%5BAutosaved%5D.pptx)
  
  <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/38ea1de2-dc5b-433c-9a40-936954e40793" alt="Image Description" width="450"><img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/24b33b02-0bbf-404e-a1f2-f89ff82e98ea" alt="Image Description" width="450">

###**DAX formulas used in POWERBI**
    
         1. To find total no of records :
                    TotalRecords = COUNTROWS('final dataset to make visual')
    
         2. To find max Reaction Type count :
                    reaction_type_max_Count = MAXX ( VALUES ( 'final dataset to make visual'[Reaction Type] ), CALCULATE ( COUNTROWS ( 'final dataset to make visual' ) ) )
    
         3. To find most frequent Reaction Type :
                    MostFrequentReaction = 
                             VAR MaxCount = 
                                  MAXX(
                                      VALUES('final dataset to make visual'[Reaction Type]), 
                                      CALCULATE(COUNTROWS('final dataset to make visual'))
                                       )
                              RETURN
                                  MAXX(
                                      FILTER(
                                           ADDCOLUMNS(
                                                 VALUES('final dataset to make visual'[Reaction Type]),
                                                 "TypeCount", CALCULATE(COUNTROWS('final dataset to make visual'))
                                                 ),
                                           [TypeCount] = MaxCount
                                          ),
                                     'final dataset to make visual'[Reaction Type]
                                   )
    
          4. To find most commonly repeated month
                   MostFrequentMonths = 
                           VAR MaxCount = 
                                   MAXX(
                                       VALUES('final dataset to make visual'[Month_name]), 
                                       CALCULATE(COUNTROWS('final dataset to make visual'))
                                        )
                           VAR FrequentMonths = 
                                    FILTER(
                                        ADDCOLUMNS(
                                              VALUES('final dataset to make visual'[Month_name]),
                                              "MonthCount", CALCULATE(COUNTROWS('final dataset to make visual'))
                                               ),
                                        [MonthCount] = MaxCount
                                        )
                                   RETURN
                                               CONCATENATEX(FrequentMonths, 'final dataset to make visual'[Month_name], ", ")



- **Presentation File**: [Accenture_SocialBuzz_Presentation.pptx](Data Analytics template - Task 3_final [Autosaved].pptx)
  
  <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/c32dc23e-4692-4fe6-8fa2-5458d1a191e3" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/f919c55d-d08d-42c8-83e7-6fecdd1a17e8" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/f663b538-4223-431a-86db-cd2d8c59d53e" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/00ec02ff-024b-413f-b17b-cd8b91a37f37" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/2d00cbb7-f5ff-4843-a8b9-cac3952b3a9a" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/9c510013-bea1-481b-9a89-5a2ce05dbfa7" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/095e6b2c-404e-43b5-a438-91056516a4ac" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/3f636e02-c612-4991-9bc1-e7f0bae5c928" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/711d5557-401e-43a2-97d6-ca4846a5fc5a" alt="Image Description" width="300">  <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/6ec36e89-e29f-4073-9734-0858668c52df" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/94f57fef-dd7a-4e81-99b5-c6ea5ce9d64a" alt="Image Description" width="300">   <img src="https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/071e165f-f3d0-4a9f-80b3-14cc4365f356" alt="Image Description" width="300">

- **Storytelling Video**: [![Watch the video](https://github.com/madulika-prabu/Accenture-SocialBuzz-Job-Simulation/assets/131234604/c03f5603-6676-4233-8deb-5fbd37b56c25)](video_url)

Caption of this video content :

Good morning all.  It's a pleasure to present the findings from our comprehensive analysis of Social Buzz's content data. As we discussed earlier, understanding your platform's top-performing categories and user engagement trends is crucial for enhancing your content strategy and solidifying your position as a leading social media platform.

Before delving into the specifics, I'd like to commend Social Buzz's remarkable growth and success over the past few years. Reaching over 500 million active users each month is a testament to the platform's appeal and the quality of the content it hosts.

Now, let's explore the key insights we've uncovered:

Our analysis revealed that from the total of 16 categories, the top five categories resonate strongly with users, generating the highest engagement scores they are Animals, Science, Healthy Eating, Technology, Food. Among these top categories, the "Animals" category emerged as the clear frontrunner, closely followed by "Science." This finding suggests that your user base has a significant affinity for content related to animals and scientific topics, captivating their attention and aligning with their interests.
As you can see from this chart, the "Animals" category consistently outperformed others, indicating its widespread popularity among your users.

As depicted in the line graph illustrating the year-over-year performance Despite overall content engagement growth from 2020 to 2021, there was a slight moderation across all categories compared to their exceptional performance in 2020. This trend suggests evolving user preferences, potential seasonal influences, or content saturation within popular categories. However, this moderation also presents an opportunity to explore areas for improvement, such as content diversification or targeted marketing campaigns, to rejuvenate user interest and satisfaction on the Social Buzz platform. This could be a sign that users are craving something fresh, a new adventure on the Social Buzz safari!

Remarkably, the sentiment analysis revealed that approximately 70% of the posts across all categories conveyed positive sentiment. This finding highlights the positive and uplifting nature of the content on your platform, fostering a constructive and engaging environment for your users.

  In addition to analyzing content categories, we also examined the type of content created by users. Interestingly, our findings indicate that photo content has a higher creation rate compared to video content. This insight suggests that users may find it easier or more convenient to create and share photo-based content on the platform.By focusing on enhancing the user experience for photo content creation and sharing, we can cater to this preference and potentially drive even higher engagement levels.
  
From the bar chart illustrating monthly engagement patterns which uncovered that May and January experienced the highest levels of content creation and user engagement. This pattern could be influenced by seasonal factors, cultural events, or user behavior during specific times of the year.By capitalizing on these peak activity periods, we can strategically align content releases, promotional campaigns, and user engagement initiatives to maximize their impact and resonate with your user base.

Diving deeper into category-specific impressions, which is been visualized in form of a heatmap , the analysis revealed that the "Animals" category elicited a higher impression of "Scared," while "Healthy Eating" and "Technology" garnered stronger impressions of "Adore." The "Science" category resonated with the impression of "Want," and "Food" content evoked feelings of "Hate" among users.By understanding these nuanced impressions, we can fine-tune our content presentation, messaging, and user experiences tailored to resonate with the unique sentiments associated with each category, further enhancing user engagement and satisfaction.

In summary, our analysis has uncovered valuable insights into your platform's content landscape, user preferences, and engagement dynamics. By leveraging these findings, we can strategically tailor our content offerings, enhance user experiences, and solidify Social Buzz's position as a leading social media platform.

Moving forward, I recommend focusing on the following areas:

1. Explore innovative content formats and themes within these categories to keep users captivated and foster sustained growth.
2. Analyze the moderation in 2021 performance to identify potential areas for improvement, such as content diversification or targeted marketing campaigns.
3. Capitalize on the monthly engagement patterns by aligning content releases, promotional campaigns, and user engagement initiatives with peak activity periods.
4. Utilize the category-specific impression data to fine-tune content presentation, messaging, and user experiences tailored to resonate with the unique sentiments associated with each category.
5. By collaborating with relevant influencers and creators, we can amplify the reach and impact of our content, tapping into their established follower bases and leveraging their credibility to drive engagement further.

By implementing these recommendations and continuously monitoring user engagement metrics, Social Buzz can solidify its position as a market leader and deliver an unparalleled social media experience to its users.

I am confident that these insights and strategies will contribute significantly to Social Buzz's continued success and growth. I look forward to discussing these findings in greater detail and collaborating with you to develop a comprehensive content strategy that propels your platform to new heights.

Thank you for your time and attention. I'm happy to address any questions or clarifications you may have.


## Conclusion

By following these steps and leveraging the provided data sets and model, you can effectively analyze social media trends and identify the top-performing categories. 
