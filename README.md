# Airbnb_Readme

<aside>
👉 This project is a part of Nanodegree of Udacity. I will follow the principle of CRISP-DM to create a pipeline for the data science project.

</aside>

[GitHub - Ashes814/Airbnb](https://github.com/Ashes814/Airbnb.git)

# CRISP-DM

## 1. Business Understanding

<aside>
💡 As an GISer, I will pay attention to the spatial distribution of listings and its connection.

</aside>

- Where has the highest/lowest prize for a list, and what is the reason of such distribution.
- How well can we predict a list' s review score? What aspects correlate well to list satisfaction?

## 2. Data Understanding

Let me introduce the data first. We have two datasets *listings* and *neighbourhoods.* Datasets include the details of Aribnb hosts information in **Shanghai, CHINA.**

We can divide our dataset into four parts.

- **Hosts information**
    - Includes host personal information, hosts name, listings count, superhost and so on.
- **Location**
    - Latitudes and longitudes of each lists (WGS84).
    - Neighbourhood information
- **Room property**
    - Room availability, amenities, type...
- **Review scores**
    - Six dimensions - *accruacy, cleanliness, checkin, communication, location, and value.*
    - Rating - Integrate review score.

## 3. Prepare Data

We will remove redundant information and working with categorical and missing data in this part.

- **Remove redundant information**
    - Only information related with our business understanding questions are kept with.
    - Big fields such as the review detail by customers are removed.
- **Categorical data**
    - We used one-hot coding to code categorical data.
- **Missing data**
    - For the problem1, we will have about 28125 non-missing data because price and location information are the basic information of a list.
    - For the problem2, we just collect about 17000 non-missing data because some customers won’t give any review score. We will treat those data as *no score* instead of simply deleting because we want to find why they weren’t give the score.

## 4. Model Data

We implemented two kinds of model for our business problem:

- **Spatial analysis**
    - Spatial auto-correlation and Hot spot analysis.
- **Supervised regression**
    - Powerful machine learning methods help us predicting the review score.
    - We will implement Linear Regression (LR), SVM, RF, etc. Comparing its performance and trying to explain it.

## 5. Results

- We will give answers for our business understanding.
- Some useful advices will also be our results due to our findings.

## 6. Deploy

- A jupyter notebook contains all the data processing procedure we have made in this project.
- A solution blog for our findings.
- A GitHub repository for all related files.

# Introduction

![Untitled](Airbnb_Rea%208856b/Untitled.png)

Airbnb, founded in 2008, makes money by charging guests and hosts for short-term rental stays in private homes or apartments booked through the Airbnb website. It started in prototype in San Francisco and expanded rapidly, and is now operating in hundreds of cities around the world.

About twenty-five million people live in Shanghai, one of the biggest cities in China, which has a huge market for renting house. We use basic map visuallisation and data analysis skills to show your the host distribution of Airbnb in Shanghai.

![heatplot.jpg](Airbnb_Rea%208856b/heatplot.jpg)

![listings.jpg](Airbnb_Rea%208856b/listings.jpg)

![var_boxplot.jpg](Airbnb_Rea%208856b/var_boxplot.jpg)