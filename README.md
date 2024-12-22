# -Olympics-Data-Analysis-Using-SQL

## Description
-SQL Case Study: Olympics Data Analysis
-The case study focuses on analyzing two datasets, olympics and olympics_noc, to extract insights related to the Olympic Games. Various SQL queries are crafted to address questions such as:
-Count andList of Olympic Games: Determining the total number of Olympic Games held and listing all the games with their respective years, seasons, and host cities.
-Participation Analysis: Calculating the total number of nations participating in each Olympic Game and identifying the games with the highest and lowest participation.
-Country and Sport Insights: Identifying nations that participated in all Olympic Games and sports played in all Summer Olympics or only once across all games.
-Sport Analysis per Game: Fetching the total number of sports played in each Olympic Game and analyzing the sports played just once.
-Athlete Analysis: Identifying the oldest gold medalist, calculating the gender ratio of athletes, and listing the top athletes with the most medals.
-Medal Distribution: Listing the total gold, silver, and bronze medals won by each country, per Olympic Game, and identifying which country won the most medals in each category for every game.

##  **objective**
1.Analyze the distribution of Olympic medals across different countries and years.
2.Identify the top-performing countries and athletes based on medal counts.
3.List and analyze Olympic events based on year, country, and event type.
4.Explore the trends in participation across different Olympic Games, including changes in the number of events and athletes.
5.Categorize Olympic data based on specific criteria like age groups, gender, and athlete achievements.

## **Requirements**
Make sure you have the following installed:
- PostgreSQL (Version [e.g., 14+])
- pgAdmin or any SQL editor (optional but recommended)

## **schema**
CREATE SCHEMA public;

CREATE TABLE public.olympics (
    id INT PRIMARY KEY,        -- Athlete ID
    name VARCHAR(255),         -- Athlete's Name
    sex CHAR(1),               -- Sex (M/F)
    age INT,                   -- Age of Athlete
    height DECIMAL(5, 2),      -- Height of Athlete (e.g., 180.25)
    weight DECIMAL(5, 2),      -- Weight of Athlete (e.g., 75.5)
    team VARCHAR(255),         -- Team Name (Country or Group)
    noc VARCHAR(3),            -- National Olympic Committee Code (e.g., USA, IND)
    games INT,                 -- Number of Games
    year INT,                  -- Year of the event
    season VARCHAR(6),         -- Season (e.g., 'Summer' or 'Winter')
    city VARCHAR(255),         -- City where the event took place
    sport VARCHAR(255),        -- Sport played (e.g., 'Basketball')
    event VARCHAR(255),        -- Event name (e.g., 'Men's Basketball')
    medal VARCHAR(10)          -- Medal earned (e.g., 'Gold', 'Silver', 'Bronze', 'None')
);

second table:
CREATE TABLE public.olympics_noc (
    noc VARCHAR(3) PRIMARY KEY,  -- National Olympic Committee Code (e.g., USA, IND)
    region VARCHAR(255),         -- Region or Continent (e.g., North America, Asia)
    notes TEXT                   -- Additional notes about the NOC
);


## **Dataset**
The data for this project is sourced from the Kaggle dataset:
DATASET=https://www.kaggle.com/datasets/heesoo37/120-years-of-olympic-history-athletes-and-results?select=noc_regions.csv
