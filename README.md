# A4_data_preparation

**A. 5 Day Data Cleaning Challenge by Rachel Tateman:**

https://www.kaggle.com/iramshiv/data-cleaning-challenge-handling-missing-values

https://www.kaggle.com/iramshiv/data-cleaning-challenge-scale-and-normalize-data

https://www.kaggle.com/iramshiv/data-cleaning-challenge-parsing-dates

https://www.kaggle.com/iramshiv/data-cleaning-challenge-character-encodings

https://www.kaggle.com/iramshiv/data-cleaning-challenge-inconsistent-data-entry

**B. Trifacta :**

Imported "PlayList" dataset from (https://www.kaggle.com/c/nfl-playing-surface-analytics/data)

**Errors & Problems**

*Missing Values*

This dataset have null values in following fields as below,

![Missing Values](https://github.com/iramshiv/A4_data_preparation/blob/master/MissingValues.jpg)

*Play Type*

when analysed the dataset, it seems like missed to enter the data.

![before_play](https://github.com/iramshiv/A4_data_preparation/blob/master/playType_before.jpg)

Solution: 

null values in PlayType column will be filled down with last valid value. After Cleaning,

![after_play](https://github.com/iramshiv/A4_data_preparation/blob/master/playType_after.png)

*null values in StadiumType, Weather columns will be added to unknown type.*

**Inconsistent data**

*Stadium Type*

There are 30 different stadium types in the dataset,

![stadium type](https://github.com/iramshiv/A4_data_preparation/blob/master/stadium.jpg)

When we inspect these levels, we can see that there are minor differences in the description of these values, in addition to spelling errors.

![before_stadium](https://github.com/iramshiv/A4_data_preparation/blob/master/1.%20stadiumType_before.png)

solution:

We’ll clean these up to 7 distinct types,
  1. indoor_close
  2. indoor_open
  3. outdoor
  4. retract_roof
  5. dome_open
  6. dome_close
  7. unknown

After clean up, ![Clean_Stadium](https://github.com/iramshiv/A4_data_preparation/blob/master/1.%20stadiumType_after.jpg)

*Weather*

Similarly the weather.

In the raw data provided, there are 64 different weather types categorised,

![weather_data](https://github.com/iramshiv/A4_data_preparation/blob/master/weather.jpg)

Before Cleaning,

![before_weather](https://github.com/iramshiv/A4_data_preparation/blob/master/2.%20weather_before.jpg)

solution:

I will also condense these in to five groups,
  1. clear
  2. overcast
  3. rain
  4. snow
  5. none
  6. unknown

![after_weather](https://github.com/iramshiv/A4_data_preparation/blob/master/2.%20weather_after.jpg)

**Recipe**

Stadium Type & Weather:

![reciepe](https://github.com/iramshiv/A4_data_preparation/blob/master/recipe.jpg)

Play Type:

![play_recipe](https://github.com/iramshiv/A4_data_preparation/blob/master/play_recipe.jpg)

Recipe also uploaded as trifacta .wrangle file,
  1. PlayList(weather).wrangle : 
      https://github.com/iramshiv/A4_data_preparation/blob/master/PlayList%20%20(weather).wrangle
  2. PlayList(play).wrangle : 
      https://github.com/iramshiv/A4_data_preparation/blob/master/PlayList%20(play).wrangle





