# This is a portfolio of all the Data Science projects I have completed

## [Project 1: Glassdoor-Salary-Analysis](https://github.com/MarlinMyrte/Glassdoor-Salary-Analysis)

- Created a tool that estimates mainly Salaries using Glassdoor.com data based on keyword search using python and selenium. The tools is mainly designed for Data Science related jobs.
- For scraping the website, the code from [this](https://towardsdatascience.com/selenium-tutorial-scraping-glassdoor-com-in-10-minutes-3d0915c6d905) article was used as a base. However, the code was outdated and presented a lot of bugs so I fixed extensively
- The scraper collects by default 180 job listings from Glassdoor. After that limit, Glassdoor keeps repeating the same jobs listings.
- Extracted keywords from the job description in order to quantify the value that each skill adds to the salary.
- Optimized Linear, Lasso and Random Forest Regressors using GridsearchCV to reach the best model

![](/Images/Wordcloud.png)


## [Project 2: Titanic Dataset](https://github.com/MarlinMyrte/Titanic-Dataset)

My submission for the Kaggle Titanic competition

Accuracy 78.47% - Top 17%

- Performed preprocessing on the dataset by parsing columns or creating new features
- Performed Exploratory Data Analysis
- Tested various Machine Learning models
- Further tuned the models and created ensembles
- Submitted the results


## [Project 3: NBA: First minutes of a game (Part 1)](https://github.com/MarlinMyrte/First-Minutes-Part-1)

In this project I wanted to test something that I had observed while watching NBA Games. I noticed that during the first 2-3 minutes of each quarter, players seem more "relaxed" compared to the rest of the quarter and I wanted to check if my hypothesis is True or not

This project involved:
- Extracting Play-by-Play data from the NBA API
- Cleaning the data and performing some feature engineering
- Plotting results to check for patterns
- Testing multiple statistical hypotheses

### Results

![](/Images/ppm_avg.png)

We can see that there is indeed a drop in the combined point production during the first minutes of each quarter, however it bounces back fairly quickly.

The statistical test confirms our initial hypothesis that there is a difference between the offensive performance during the first 2 minutes of each quarter.

But why does this happen? Is it affected by the pace of the game? Let's check the possessions per minute

![](/Images/poss_ppm_avg.png)

We also found out that teams perform better offensively in the first half mainly because there are more possessions in the first half than in the second half.

## Project 4: NBA: First minutes of a game (Part 2) - Coming Soon
