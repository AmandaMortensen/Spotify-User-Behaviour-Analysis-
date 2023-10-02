# Spotify-User-Behaviour-Analysis-
Data analysis in Python using pandas, matplotlib, seaborn and NumpPy. Please see the attached Juputyer Noterbook for the full code and visulisations.

### **Situation**
Being a daily user Spotify, one of the world's leading music streamning platforms, I became curious to know more gaining insight into the sentiment of the wider Spotify audience. Hence, I embarked on conducting a user bahviour analysis of Spotify. 

### **Task**

The aim of the task was to gain insight into the user sentiment of various Spotify offerings, such as their subscription plans and podcasts, alongside with acheiving a firm understaning of the how Spotify users (across ages and gender) usages Spotify. All with the aim of outlining impactful insights and recommendations for how Spotify could improve user experience and user rention.

### **Action**

For my data analysis, I followed the following steps:

1. Data Exploration
2. Data Cleaning
3. Data Analysis 
- Understanding ditribution of certain behaviours according to age and gender
- Insight into music recommendation ratings, listening frequency and prefered devices
- Analsysis of Spotify's podcast offering

### **Results**

#### **Insights** 
1. Maximum number of the users are of the age range 20-35 and are females
2. Most users have been users for more than 2 year and is predominant females age 20-35
3. Smart Speakers and Voice Assistants are the most used devices and wearable devices are the least used devices
4. Most of the females are using 'free plan, and so are males - with females being most likely to switch to premimum
5. The most prefered premium plan is the family plan
6. Melody is the prefered music genre
7. Melody songs are most preferred at night and morning, and classical in afternoon.
8. In 'Sadness or Melancholy' mood and in leisture time most of the people listen music through Spotify
9. Most of the people rate spotify recommendations as '3 out of 5'
10. Maximum number of people love to listen comedy podcasts
11. Maximum number of people like shorter podcasts and rate 'ok' for the variety and availabilty of podcasts


#### **Recommendations** 

1. Look further into what factor has the strongest correlation to the good retention rate (point 2)
2. Potentially collaborate with any smart speaker or voice assitant device company, to enhance the connectability (point 3)
3. Develop a strategy for increasing males' willingness to switch to a premium plan (point 4)
4. Improve variety and availabiity of podcats, ideally within the comedy area (point 11) 
   

### **Code Preview** 

Importing data 

```

import numpy as np
import pandas as pd
from matplotlib import pyplot as plt 
import seaborn as sns
plt.style.use('ggplot')
import matplotlib.pyplot as plt 

from PIL import Image
from wordcloud import WordCloud
from nltk.corpus import stopwords 
```
Load data

```
df = pd.read_csv('/Users/amandamortensen/Desktop/Data Analytics/Python Projects/Project 3 /Spotify_data.csv')```
```

Spotify User Analysis - distribution of spotify users by age (bar chart)

```
df['Age'].unique()

```

```
plt.hist(df.Age, color='Green')
plt.show 
plt.title('Disitribution of Spotify Users by Age')
plt.xlabel('Age')
plt.ylabel('Count')
```

Spotify User Analysis - distribution of Spotify users by gender (pie chart)

```
df['Gender'].unique()
```

```
x = df['Gender'].value_counts()
plt.pie(x,autopct= '%1.1f%%')
plt.show 
labels = ['female', 'male', 'others']
plt.legend(labels)
plt.show
plt.title('Distribution of Spotify Users by Gender')
```

Spotify User Experience Analysis - Music Recommendation Ratings (violin plot)

```
sns.violinplot(x=df["music_recc_rating"])
plt.xlabel('Count')
plt.ylabel('Ratings')
plt.title('Distrubution of how Users Rate the Spotify Music Recommendations')
```


