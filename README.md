# TalkingData-Fraudulent-Click-Prediction

# Understanding the Business Problem

TalkingData is a Chinese big data company, and one of their areas of expertise is mobile advertisements.

In mobile advertisements, click fraud is a major source of losses. Click fraud is the practice of repeatedly clicking on an advertisement hosted on a website with the intention of generating revenue for the host website or draining revenue from the advertiser.

In this case, TalkingData happens to be serving the advertisers (their clients). TalkingData cover a whopping approx. 70% of the active mobile devices in China, of which 90% are potentially fraudulent (i.e. the user is actually not going to download the app after clicking).

You can imagine the amount of money they can help clients save if they are able to predict whether a given click is fraudulent (or equivalently, whether a given click will result in a download).

Their current approach to solve this problem is that they've generated a blacklist of IP addresses - those IPs which produce lots of clicks, but never install any apps. Now, they want to try some advanced techniques to predict the probability of a click being genuine/fraud.

In this problem, we will use the features associated with clicks, such as IP address, operating system, device type, time of click etc. to predict the probability of a click being fraud.

They have released the problem on Kaggle here..
Understanding and Exploring the Data

The data contains observations of about 240 million clicks, and whether a given click resulted in a download or not (1/0).

On Kaggle, the data is split into train.csv and train_sample.csv (100,000 observations). We'll use the smaller train_sample.csv in this notebook for speed, though while training the model for Kaggle submissions, the full training data will obviously produce better results.

# The detailed data dictionary is mentioned here:

    * ip: ip address of click.
    * app: app id for marketing.
    * device: device type id of user mobile phone (e.g., iphone 6 plus, iphone 7, huawei mate 7, etc.)
    * os: os version id of user mobile phone
    * channel: channel id of mobile ad publisher
    * click_time: timestamp of click (UTC)
    * attributed_time: if user download the app for after clicking an ad, this is the time of the app download
    * is_attributed: the target that is to be predicted, indicating the app was downloaded

Let's try finding some useful trends in the data.


# Packages

1. numpy
2. pandas
3. matplotlib
4. seaborn
5. scikit learn 
6. xgboost

