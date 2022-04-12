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

![](/Images/poss_pm_avg.png)

We also found out that teams perform better offensively in the first half mainly because there are more possessions in the first half than in the second half.

## [Project 4: NBA: First minutes of a game (Part 2)](https://github.com/MarlinMyrte/First-Minutes-Part-2)

We discovered that there are teams which have a larger difference in their offensive performance in the first 2 minutes of each quarter compared to their offensive performance in the first 10 minutes of each quarter.

![](/Images/Top%20Bottom%20diff.png)

**So what if this "2-minute slump" didn't exist? How would the standings be different?**

Please note that the standings are as of February 28th 2022.

![](/Images/Full_Standings.png)

In the Eastern Conference, we can see that the 76ers jumped from the 3rd place to the 2nd place which is something that could change a lot during the Playoffs and also the Wizards went up to the 10th place

Ιn the Western Conference, the Lakers moved up a spot and are in the playoff picture and the Clippers are in the play-in tournament

**As we know, even small changes in the seeding of the teams might have a significant impact in determining the NBA Champion. Therefore, it is of high interest for the teams to try and tackle this "2 minute slump"**

## [Project 5: NBA: Predicting the winner of the Most Improved Award](https://github.com/MarlinMyrte/Most-Improved-Player-Prediction)

The MIP award is probably my favourite award among all the other ones as it is given to the player who has put the most effort in improving his game and has reached a new level on the way he's playing. It is a reward for all the dedication and the effort that was put into training and improving. It is not only about improving your individual stats but also the impact you make on the court, how the defense perceives you and makes adjustments for you and the value you add to your team. Usually winners of the MIP go on to become All Stars and NBA Champions. This year, the top 5 candidates according to many websites are Ja Morant, Darius Garland, Miles Bridges, Desmond Bane and Dejounte Murray with Ja Morant emerging as the number 1 favorite. In many occassions narratives built around those players and hype play a major role in the process of giving out these awards. Let's see if the numbers support these candidacies and if the hype is real.

In this project I:
- Created a pipeline to extract data from basketballreference.com using BeautifulSoup
- Cleaned the data and performed all necessary transformations
- Tried to predict the winner of the 2022 MIP award using 2 methods (Classification & Regression)
- Performed ensembles of the best methods to come up with predictions

This problem can be approached from 2 different perspectives. The first one is to try to make a prediction by using a **classification model**. In this case the target variable in our training set is either 1 (for winners of the award) or 0 (for the candidates that season).

The other one is **regression**. We can turn this classification problem into a regression one. Instead of trying to predict the class of each player we can try to predict the votes he will get and more specifically the votes share he will get. We have data for the voting results from the previous years and we will use them as our target variable.

For both methods I tried different approaches like scaling the data, oversampling and percentile ranks.
The best performing datasets for the classification approach were:

![](/Images/clf_accuracies.png)

And as for the regression approach:

![](/Images/reg_accuracies.png)

And now the predictions:

**Classification**

![](/Images/clf_pred.png)

The classification algorithm predicted Dejounte Murray as the winner. As we can see, 2 out of the top 5 candidates appear in the predictions. We can also see Obi Toppin, Tyrese Maxey and Josh Hart making an appearance. All of them have made significant improvements in their game this season and have been getting a lot more playing time too. However, they are not the leaders on their teams or play a significant role in their team's success and that's why they might not be considered favorites by the media.

**Regression**

![](/Images/reg_pred.png)

In the regression results, 4 out of the 5 favorites appear, however Tyrese Maxey emerges as the winner. Also, we have the clear favorite Ja Morant appear as 3rd in these standings.

**This goes to prove that our perception, media narratives and hype may not agree with what the data has to say. In both cases, Ja Morant, who has been stellar this season and is even considered as an MVP candidate, did not emerge as the winner of the Most Improved Award. On the other hand, there are players who numerically have improved more and who will probably get less recognition for that achievement because they don't have a star status or they do not currently lead their teams.**
