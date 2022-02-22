## **DATASET**
Kaggle link : https://www.kaggle.com/c/cascade-cup-22/data

## **FEATURE ENGINEERING**
### **New features added**

Average_mile_distance : Average distance the rider has to cover to deliver the order

diff1 : Timestamps difference between allot_time and order_time

diff2 : Timestamps difference between accept_time and order_time

Reassignment_method was encoded as follows:

reassignment_method ={'auto':1 ,'manual':2 ,'nan':3}

order_day and month: Day and month on which the order was placed

riders: Frequency of orders alloted to each rider in train and test dataset

order_change_final : Binary encoding of change in undelivered orders of a particular rider

## **MODEL**

The dataset was trained on catboost model and the AUC on validation data was around 0.95.

AUC on private dataset : 0.90134


