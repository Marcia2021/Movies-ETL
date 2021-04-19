# Movies-ETL Analysis

## Overview of the Movies-ETL

Extract, Transform and Load (ETL) is a data pipeline moves data from a source to a destination. The ETL process creates data pipelines that also transform data along the way. In this module we extracted data from both Wikipedia and Kaggle, transformed the datasets by cleaning them and joining them together, then loaded the cleaned dataset into a SQL database.

In order to repeat the perform of this ETL process, we are going to create an automated pipeline that takes in new data, performs the appropriate transformations, and loads the data into existing tables. There are four tasks:
-	Write an ETL Function to Read Three Data Files
-	Extract and Transform the Wikipedia Data
-	Extract and Transform the Kaggle data
-	Create the Movie Database

## Analysis
1.	Write an ETL Function to Read Three Data Files:
    Created a function to read in the datasets. For each of these datasets, converted them to a DataFrame.
    
    In the next steps, we are going to clean up the Wikipedia data and Kaggle data. 
    
2.	Extract and Transform the Wikipedia Data:
    In the function created from step1, added steps to transform the Wikipedia data by cleaning and filtering data with list comprehension, removing duplicates with regular         expressions, removing columns with null values, dropping null values and converting data to string values. Additionally, clean the box office, budget, release date and           running time to be able to get the final cleaned data.
    
3.	Extract and Transform the Kaggle data

    There are two datasets from Kaggle data: movie-metadata and ratings. Used regular expression to clean up both files. Then merged the Kaggle data with the Wikipedia data from     step2. Dropped unnecessary columns, filled in missing Kaggle data. 
    
4.	Create the Movie Database:
    Created Database in PostgreSQL. Created the connection to the PostgreSQL database, added the final dataframe created from step3 to the SQL database. 
    
## Results

1.	There are 3 DataFrame created from step1:

    Wiki_movies_df sample:

    ![inst1](https://user-images.githubusercontent.com/79289806/115178708-dfce1000-a09f-11eb-9fdf-8ada66384dcf.png)

    Kaggle_metadata sample:

    ![inst2](https://user-images.githubusercontent.com/79289806/115178710-dfce1000-a09f-11eb-824d-a549cb410566.png)
 
    Kaggle ratings data sample:

    ![inst3](https://user-images.githubusercontent.com/79289806/115178703-df357980-a09f-11eb-80b4-8ae81ae2fbde.png)

2.	Cleaned wiki_movies_df sample:

    ![inst4](https://user-images.githubusercontent.com/79289806/115178704-df357980-a09f-11eb-8a65-a8ceb68352fc.png)

3.	Final merged dataset sample:

    ![inst5](https://user-images.githubusercontent.com/79289806/115178705-df357980-a09f-11eb-8894-8d7631dfda46.png)

4.	Upload the movies and ratings data to PostgreSQL database:

    ![inst6](https://user-images.githubusercontent.com/79289806/115178706-dfce1000-a09f-11eb-9e8b-22db0f10bae7.png)

    ![inst7](https://user-images.githubusercontent.com/79289806/115178707-dfce1000-a09f-11eb-9f59-c1fceeadfe39.png)    

## Summary: 

The ETL process helped us the set up the plan for the initial process of the data analysis. We could extract data from different resources, clean up the data along the way, and connect different programming platforms to better process and analyze the data in the following steps. 



