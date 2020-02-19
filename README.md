![MarketSegmentation](https://ciriusmarketing.com/wp-content/uploads/2019/10/market-segmentation.jpg)


## **Introduction**

This study seeks to identify unique clusters of young people based on their responses to a lifestyle and interests survey. It uses unsupervised clustering algorithms (k-Means) and dimensionality reduction (PCA, tSNE) to arrive at the cluster assignments.  
  
## **Hypothesis**   
* We can find new or unexpected ways to group young adults, based on latent patterns in their survey responses.  
* We can distill the survey questions down to essential vectors that encapsulate the information contained in their responses. 
   
## **The Data**

[Data Source](https://www.kaggle.com/miroslavsabo/young-people-survey)

In 2013, students of the Statistics class at FSEV UK were asked to invite their friends to participate in this survey.  

The data file (responses.csv) consists of 1010 rows and 150 columns (139 integer and 11 categorical).  
For convenience, the original variable names were shortened in the data file. The columns.csv file provides the abridged column names mapped to the original column names.   
The data contain missing values.  
The survey was presented to participants in both electronic and written form.  
The original questionnaire was in Slovakian and was later translated into English.  
All participants were of Slovakian nationality, aged between 15-30.  
The variables can be split into the following groups:  
  
Music preferences (19 items)  
Movie preferences (12 items)  
Hobbies & interests (32 items)  
Phobias (10 items)  
Health habits (3 items)  
Personality traits, views on life, & opinions (57 items)  
Spending habits (7 items)  
Demographics (10 items)  
Research questions  
 
  
**Questionnaire**  
  
MUSIC PREFERENCES  
I enjoy listening to music.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I prefer.: Slow paced music 1-2-3-4-5 Fast paced music (integer)  
Dance, Disco, Funk: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Folk music: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Country: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Classical: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Musicals: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Pop: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Rock: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Metal, Hard rock: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Punk: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Hip hop, Rap: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Reggae, Ska: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Swing, Jazz: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Rock n Roll: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Alternative music: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Latin: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Techno, Trance: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Opera: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
  
MOVIE PREFERENCES  
I really enjoy watching movies.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
Horror movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Thriller movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Comedies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Romantic movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Sci-fi movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
War movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Tales: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Cartoons: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Documentaries: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Western movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
Action movies: Don't enjoy at all 1-2-3-4-5 Enjoy very much (integer)  
  
HOBBIES & INTERESTS  
History: Not interested 1-2-3-4-5 Very interested (integer)  
Psychology: Not interested 1-2-3-4-5 Very interested (integer)  
Politics: Not interested 1-2-3-4-5 Very interested (integer)  
Mathematics: Not interested 1-2-3-4-5 Very interested (integer)  
Physics: Not interested 1-2-3-4-5 Very interested (integer)  
Internet: Not interested 1-2-3-4-5 Very interested (integer)  
PC Software, Hardware: Not interested 1-2-3-4-5 Very interested (integer)  
Economy, Management: Not interested 1-2-3-4-5 Very interested (integer)  
Biology: Not interested 1-2-3-4-5 Very interested (integer)  
Chemistry: Not interested 1-2-3-4-5 Very interested (integer)  
Poetry reading: Not interested 1-2-3-4-5 Very interested (integer)  
Geography: Not interested 1-2-3-4-5 Very interested (integer)  
Foreign languages: Not interested 1-2-3-4-5 Very interested (integer)  
Medicine: Not interested 1-2-3-4-5 Very interested (integer)  
Law: Not interested 1-2-3-4-5 Very interested (integer)  
Cars: Not interested 1-2-3-4-5 Very interested (integer)  
Art: Not interested 1-2-3-4-5 Very interested (integer)  
Religion: Not interested 1-2-3-4-5 Very interested (integer)  
Outdoor activities: Not interested 1-2-3-4-5 Very interested (integer)  
Dancing: Not interested 1-2-3-4-5 Very interested (integer)  
Playing musical instruments: Not interested 1-2-3-4-5 Very interested (integer)  
Poetry writing: Not interested 1-2-3-4-5 Very interested (integer)  
Sport and leisure activities: Not interested 1-2-3-4-5 Very interested (integer)  
Sport at competitive level: Not interested 1-2-3-4-5 Very interested (integer)  
Gardening: Not interested 1-2-3-4-5 Very interested (integer)  
Celebrity lifestyle: Not interested 1-2-3-4-5 Very interested (integer)  
Shopping: Not interested 1-2-3-4-5 Very interested (integer)  
Science and technology: Not interested 1-2-3-4-5 Very interested (integer)  
Theatre: Not interested 1-2-3-4-5 Very interested (integer)  
Socializing: Not interested 1-2-3-4-5 Very interested (integer)  
Adrenaline sports: Not interested 1-2-3-4-5 Very interested (integer)  
Pets: Not interested 1-2-3-4-5 Very interested (integer)  
  
PHOBIAS  
Flying: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Thunder, lightning: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Darkness: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Heights: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Spiders: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Snakes: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Rats, mice: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Ageing: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Dangerous dogs: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
Public speaking: Not afraid at all 1-2-3-4-5 Very afraid of (integer)  
  
HEALTH HABITS  
Smoking habits: Never smoked - Tried smoking - Former smoker - Current smoker (categorical)  
Drinking: Never - Social drinker - Drink a lot (categorical)  
I live a very healthy lifestyle.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
  
PERSONALITY TRAITS, VIEWS ON LIFE & OPINIONS  
I take notice of what goes on around me.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I try to do tasks as soon as possible and not leave them until last minute.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always make a list so I don't forget anything.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I often study or work even in my spare time.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I look at things from all different angles before I go ahead.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I believe that bad people will suffer one day and good people will be rewarded.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am reliable at work and always complete all tasks given to me.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always keep my promises.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I can fall for someone very quickly and then completely lose interest.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I would rather have lots of friends than lots of money.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always try to be the funniest one.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I can be two faced sometimes.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I damaged things in the past when angry.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I take my time to make decisions.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always try to vote in elections.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I often think about and regret the decisions I make.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I can tell if people listen to me or not when I talk to them.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am a hypochondriac.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am emphatetic person.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I eat because I have to. I don't enjoy food and eat as fast as I can.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I try to give as much as I can to other people at Christmas.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I don't like seeing animals suffering.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I look after things I have borrowed from others.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I feel lonely in life.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I used to cheat at school.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I worry about my health.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I wish I could change the past because of the things I have done.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I believe in God.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always have good dreams.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always give to charity.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I have lots of friends.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
Timekeeping.: I am often early. - I am always on time. - I am often running late. (categorical)  
Do you lie to others?: Never. - Only to avoid hurting someone. - Sometimes. - Everytime it suits me. (categorical)  
I am very patient.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I can quickly adapt to a new environment.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
My moods change quickly.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am well mannered and I look after my appearance.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I enjoy meeting new people.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always let other people know about my achievements.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I think carefully before answering any important letters.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I enjoy childrens' company.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am not afraid to give my opinion if I feel strongly about something.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I can get angry very easily.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always make sure I connect with the right people.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I have to be well prepared before public speaking.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I will find a fault in myself if people don't like me.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I cry when I feel down or things don't go the right way.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am 100% happy with my life.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I am always full of life and energy.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I prefer big dangerous dogs to smaller, calmer dogs.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I believe all my personality traits are positive.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
If I find something the doesn't belong to me I will hand it in.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I find it very difficult to get up in the morning.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I have many different hobbies and interests.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I always listen to my parents' advice.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I enjoy taking part in surveys.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
How much time do you spend online?: No time at all - Less than an hour a day - Few hours a day - Most of the day (categorical)  
  
SPENDING HABITS  
I save all the money I can.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I enjoy going to large shopping centres.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I prefer branded clothing to non branded.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I spend a lot of money on partying and socializing.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I spend a lot of money on my appearance.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I spend a lot of money on gadgets.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
I will hapilly pay more money for good, quality or healthy food.: Strongly disagree 1-2-3-4-5 Strongly agree (integer)  
  
DEMOGRAPHICS  
Age: (integer)  
Height: (integer)  
Weight: (integer)  
How many siblings do you have?: (integer)  
Gender: Female - Male (categorical)  
I am: Left handed - Right handed (categorical)  
Highest education achieved: Currently a Primary school pupil - Primary school - Secondary school - College/Bachelor degree (categorical)  
I am the only child: No - Yes (categorical)  
I spent most of my childhood in a: City - village (categorical)  
I lived most of my childhood in a: house/bungalow - block of flats (categorical)  

**Categorical Features**  
Gender  
Left - right handed  
Education  
Only child  
Village - town  
House - block of flats  
Internet usage  
Lying  
Punctuality  
Smoking  
Alcohol   
  
## **Methodology**  
  
* Intelligently impute missing data  
* Reduce dimensionality  
    * Determine optimal number of principal components  
    * How much variance do they describe?
* Cluster using principal components
    * Determine how many clusters best describe the data
    * What is the inertia of the model?
* Examine the clusters to infer generalities  
  
### PCA 

![Gif](https://i.imgur.com/NKXVX1U.gif)

**Why?**  
* There are 150+ features in the data set 
* To capture the most important info in new axes which:
    * Maximize variance
    * Minimize error

![Imgur](https://i.imgur.com/4tN3Cf6l.png)

The explained variance seems to elbow at either 3 or 4 prinicipal components (PCs). I continued with 3 because of the advantage afforded by being able to visualize the three axes in 3D space. The fourth PC wouldn't have provided much additional explained variance. 


## **Findings**  
  
Due to the limited number of observations, it was difficult to glean nuanced market segments from the individuals represented in the data. What was clear, however, is that there is clear segmentation along gender lines. This held true for nearly every category. 

However, the methodologies employed here would doubtless serve indispensable in a more refined analysis should more data be made available. 
