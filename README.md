# Pandas Challenge

Data and instructions provided by UC Berkeley Extension Data Analytics Bootcamp.

# Introduction 

The goal of this assignment is to use my newfound Python Pandas knowledge and skills to organize data stored in a csv file into dataframes. There are two
options to choose from, and I chose Heroes of Pymoli.

# Technologies

Python Pandas

Jupyter Notebook
  - (file:///Users/yyh/Downloads/HeroesOfPymoli_jupyter_notebook.html) for proper view of the dataframes, since GitHub's rendered blob doesn't display jupyter notebook's converted numerical formatting properly in the dataframes
  - Note that I made most of the unnecessary called outputs comments, so when running the notebook, only the result dataframes are showing (except the first purchas_data is needed to be run for the other commands to work)
  - I also commented on some of my commands as notes for why they are needed
  
Conda Environment used: PythonData

# Detailed Instructions

  - Heroes of Pymoli

  - Congratulations! After a lot of hard work in the data munging mines, you've landed a job as Lead Analyst for an independent gaming company. You've been assigned the task of analyzing the data for their most recent fantasy game Heroes of Pymoli.
  
  - Like many others in its genre, the game is free-to-play, but players are encouraged to purchase optional items that enhance their playing experience. As a first task, the company would like you to generate a report that breaks down the game's purchasing data into meaningful insights.

- Your final report should include each of the following:

  - Player Count
    - Total Number of Players

  - Purchasing Analysis (Total)
    - Number of Unique Items
    - Average Purchase Price
    - Total Number of Purchases
    - Total Revenue

  - Gender Demographics
    - Percentage and Count of Male Players
    - Percentage and Count of Female Players
    - Percentage and Count of Other / Non-Disclosed

  - Purchasing Analysis (Gender)
    - The below each broken by gender
      - Purchase Count
      - Average Purchase Price
      - Total Purchase Value
      - Average Purchase Total per Person by Gender

  - Age Demographics
    - The below each broken into bins of 4 years (i.e. <10, 10-14, 15-19, etc.)
      - Purchase Count
      - Average Purchase Price
      - Total Purchase Value
      - Average Purchase Total per Person by Age Group

  - Top Spenders
    - Identify the the top 5 spenders in the game by total purchase value, then list (in a table):
      - SN
      - Purchase Count
      - Average Purchase Price
      - Total Purchase Value

  - Most Popular Items
    - Identify the 5 most popular items by purchase count, then list (in a table):
      - Item ID
      - Item Name
      - Purchase Count
      - Item Price
      - Total Purchase Value

  - Most Profitable Items
    - Identify the 5 most profitable items by total purchase value, then list (in a table):
      - Item ID
      - Item Name
      - Purchase Count
      - Item Price
      - Total Purchase Value

  - As final considerations:
    - You must use the Pandas Library and the Jupyter Notebook.
    - You must submit a link to your Jupyter Notebook with the viewable Data Frames.
    - You must include a written description of three observable trends based on the data.
    - See Example Solution for a reference on expected format.

# Files
  
  The HeroesOfPymoli folder contains:
  
    - The jupyter notebook where my codes are for creating dataframes based on the csv file
    - Written report of three observable trends from the data in docx format
    - Written report of three observable trends from the data in txt format
    - The Resources folder where the csv file is store

# Process and Credits

My first assignment using Python Pandas to clean up and created organized dataframes from a csv file (data). I used class materials and outside resources for references, asked Bootcamp's Learning Assistant App for help to complete this assignment.

1. When I was working on the Gender Demographics section, I ran into the issue of not being able to merge the unique gender count with the other dataframes, so I asked the Learning Assistant App for help. The learning assistant suggested to me the function drop_duplicates(), which worked nicely and I didn't have to use merge.

2. When I was working on the Top Spenders section, I ran into the issue of not being able to merge (again!) count pull from purchase_data's SN value_count() to the other dataframes. I tried different ways to debug the error I encountered, which was something like "you are trying to merge object and int." I tried resetting the index, but that didn't work, so I asked the Learning Assistant App for help. The learning assistant suggested to me to use "user_count = purchase_data.groupby( ["SN"].count()["Price"].rename("Purchase Count")," which allowed me to merge the user count with the other dataframes nicely.

3. Here is the list of other outside resources I used to help me complete this assignments:
  - https://www.kite.com/python/answers/how-to-count-the-number-of-rows-in-a-pandas-dataframe-in-python
  - https://www.geeksforgeeks.org/different-ways-to-create-pandas-dataframe/
  - https://stackoverflow.com/questions/19125091/pandas-merge-how-to-avoid-duplicating-columns
  - https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.drop_duplicates.html
  - https://stackoverflow.com/questions/37351172/how-to-remove-index-from-a-created-dataframe-in-python
  - https://www.dataquest.io/blog/settingwithcopywarning/
  - https://stackoverflow.com/questions/41464034/summing-multiple-rows-having-duplicate-columns-pandas/41464118
  - https://www.roelpeters.be/pandas-solve-you-are-trying-to-merge-on-object-and-int64-columns/
  - https://www.kite.com/python/answers/how-to-group-a-pandas-dataframe-by-multiple-columns-in-python
  - https://www.kite.com/python/answers/how-to-reset-the-indexing-of-a-grouped-pandas-dataframe-in-python
  - https://www.kite.com/python/answers/how-to-join-two-pandas-dataframes-on-multiple-columns-in-python
