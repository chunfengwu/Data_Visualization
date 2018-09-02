## IMDB 5000 USA Movie Data Visualization Analysis 

In order to get a better understanding of the movie industry in US,  I got a dataset from Kaggle and analyzed 5000 records of USA movie data from 1980 to 2015 in terms of movie plot key words analysis, movie revenue and profit evolution, as well as movie flops and success analysis.   
The jupyter file is also available to view in [NBviewer](http://nbviewer.jupyter.org/github/YuexiSC/data-visualization/blob/master/crunchbase_data_analysis/crunch_base_data_analysis.ipynb):  

### Table of Content

&#8195;[**1. Environment Configuration**](#1.-Environment-Configuration)


&#8195;[**2. Data Preparation**](#1.-Data-Preparation)
>[**2.1. Import Data**](#2.1.-Import-Data)  
>[**2.2. Data Information**](#2.1.-Data-Information) 

&#8195;[**3. IMDB Movie Data Exploration**](#3.-IMDB-Movie-Data-Exploration)

>[**3.1. Movie Distribution by County Originated**](#3.1.-Movie-Distribution-by-County-Originated)  

>[**3.2. Evolution of Count of Movies Over Year in USA**](#3.2.-Evolution of Count of Movies Over Year in USA)  

>[**3.3. Movie Plot Key Words Analysis**](#3.3.-Movie-Plot-Key-Words-Analysis ) 

>[**3.4. Movie Revenue and Budget Distribution**](#3.4.- Movie-Revenue-and-Budget-Distribution) 

>[**3.5. Movie Flops and Success by Genre**](#3.5.-Movie-Flops-and-Success-by-Genre ) 

>[**3.6. Movie Profitability Analysis by Genre**](#3.6.-Movie-Profitability-Analysis-by-Genre) 

>[**3.7. Movie Profitability Trending Analysis**](#3.7.-Movie-Profitability-Trending-Analysis ) 

>[**3.8. Top and Least Profitable Movies**](#3.8.-Top-and-Least-Profitable-Movies ) 

        
### Data 
This project used the following four datasets, which are available in  (**Datasource**: [IMDB data]((https://www.kaggle.com/carolzhangdc/imdb-5000))
And you can check the datasets [**Here**](https://github.com/YuexiSC/data-visualization/tree/master/crunchbase_data_analysis/datasets).


|Column Name | Describtion | Example  | 
|--|--|--|
| `Movie Title` |  Name of the Movie  |  Avatar | 
| `Title Year` |  Movie released year  |  2015 | 
| `Director Name` |  Name of the Movie Director  | James Cameron |
| `Director Facebook likes` |  Nunber of facebook like under director's facebook acount  | 563 |
| `Actor Name` |  Name of the Movie Director  | Johnny Depp |
| `Actor Facebook likes` |  Nunber of facebook like under actor's facebook acount  | 2000 |
| `Genres` |  Movie type  | Action |
| `Gross` |  Total Revenue of the Movie  | 760505000 |
| `Budget` |  Total Money spend on Movie  | 237000000 |


### Tech Stacks
The project is written in Python 3.6 with Google Colaboratory tool. We used pandas and numpy for data analysis, and used seaborn, worldcloud and matplotlib for data visualization.
```
from wordcloud import WordCloud
from google.colab import files
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
import numpy as np
import matplotlib.ticker as tick
import matplotlib.patches as mpatches
import warnings
warnings.filterwarnings('ignore')
%matplotlib inline
 ```

## Highlights 
The highlighted findings with plots from jupyter notebook are as follows: 
1. Movie Revenue and Budget Distribution  
>1.  Most movies' revenue is from 5M to 50M
>2.  The median movie Revenue is 35 million
>3.  Most movies' budget is from 5M to 50M, similar to movie revenue.
>4.  The median movie Budget is 26 million, 9 million lower then median revenue. 

![png](./pics/output_34_0_copy.png) 

2. Movie Profitability Analysis by Genre        
>1.  The top movie genres are Adventure, science fiction, and fantasy. Which means these movie types are most popular in movie theater.  
>2.  However, let’s have a look at the profit for each genre, the red color dot line. For example, the median profit of Action movie is close to zero. Even Though action movies are popular,  the movie cost is too high to have profit.  We can see that family movie has the highest profit, because family movie is less costly.  



![png](./pics/output_34_0.png)


3. Evolution of Movie Flops Ratio Over Year (USA)   
>1. The flops ratio keeps increasing.   
>2. In recent 20 year, the movie flops ratio is around 50%, which mean half movies have lost money. That means movie industry is quite risky.
  

![png](./pics/output_81_0.png)   


