# hack4fusion
Repo for all open source material of the 2019 Hack For Fusion competition

Here you can find introductory material for magnetic confinement fusion: https://docs.google.com/document/d/1PxHA52lZXj5YKEckvHMK6jDDw5qUpYCdhmEHrZcKD5A/edit?usp=sharing

Check this Google Doc for the Problem Statement: https://docs.google.com/document/d/1ZkZcFKYdf87GIIUWtcP1A4VBqLU9kHHCtdRgicbC-Cg/edit?usp=sharing

The dataset is available on Kaggle: https://www.kaggle.com/cristinarea/iap-psfc-2019-hackforfusion

Frank_Geoffrey's approach description:

We started exploring the data.

We soon noticed that many columns were missing variables and decided to do an exhaustive data cleaning.

For cleaning the data, we mainly replace the NAN values with the average value of the column, leaving the columns “intentional_disruption” and “time_until_disrupt” untouched

We remove rows = 1 under columns " intentional_disruption

Later, we created a new feature called “ip_error_frac” from “ip” and “ip_error”

We normalized the data and checked for correlations

Next, we decided to try some models but very soon we decided that we should drop some columns that seemed to don’t provide any further information to our model

Finally, we test different kind of models i.e. Logistic regression, Random Forest & GBM and compared them

The best one was a GBM + LR
