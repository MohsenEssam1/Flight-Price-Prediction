# Flight-Price-Prediction

# My Notebook consists of 5 main parts which are:
> - Data Exploration Stage. <br><br>
> - Data Cleaning Stage. <br><br>
> - Data Visualization Stage. <br><br>
> - The Machine Learning Dummy Model. <br><br>
> - Training The Model. <br><br>

## First The Summary Of The Data Exploring :
> - dataframe has 8012 rows and 11 columns. <br><br>
> - There is 1 row with nan values so I will drop it (1 row won't effect my data) <br><br>
> - There is 125 row with complete duplicates so I will drop them as it is impossible that 2 plan flights with same time and duration and price and everything !!! <br><br>
> - Date_of_Journey column should be date and I noticed that all data is in 2019 <br><br>
> - Dep_Time and Arrival_Time columns are unclean as there is different formats in them so I will change both of them to date and I will display only hours and minutes <br><br>
> - I will make new columns of Duration where it will contain hours and minutes

## Second Data cleaning :
> - I removed years and I made date by months and day only (as year is 2019 only). <br><br>
> - I will made Dep_Time and Arrival_Time as 2 rows one for hours and other for minutes. <br><br>
> - I made a feature with the name of Total_duration_minutes to help me gain more insights. <br><br>
> - I found a row with total time 5 minutes (So I dropped it). <br><br>
> - Since that Total_steps gives data about Route... then I removed Route column. <br><br>
> - I removed the only row with Nan values and I removed duplicates.

## Third data visualizing :

## I visualized categoral data using barplots and violinplots and that gave me insights : 

> - Using Google search I now knew that all this cities are in india <br><br>
> - Jet Airways Buisiness has the highest average price and highest deviation (from 45k to 80k) <br><br>
> - Relative to the source the price changes !! (if the flight from Delhi that will cost max price) <br><br>
> - Relative to the Destination the price changes <br><br>
> - By increasing number of Total_Stops the Price increase <br><br>
> - Buisness class has high variation <br><br>
> - price is significantly effected by the info of the data <br><br>
> - Most travels are at May (5) <br><br>
> - Highest tickets average prices is at March (3) <br><br>
> - Highest tickets deviation in prices is at March (3)
<br><br>

## I visualized quantitative data using regression plots and that gave me insights which are : 
##### data won't have a strong linear correlation... also I can't see there is other obvious polynomial correlations and there is no curves to fit such shapes (So I think Linear regression will be a bad choice Model)

## Fourth The Machine Learning Dummy Model : 

#### Knowing that the Linear regression will be a bod choice algoithm, I used it as my baseline model <br> Where it should be my min. accuracy

## Fifth Training The Model :

##### I trained model pipeline containing model algorithms then I choosed the best accuracy <br> At the end I used RandomForest as my algorithm and that made me get 700 mae score on Kaggle
