## **FEATURE ENGINEERING**

**Features that are already present in the dataset**
order_id : unique id for each order

order_time: time of the creation of order by the client

order_date : date of the order

allot_time: time of allocation of order to the rider
accept_time: time of acceptance of the order by the rider (if available)
pickup_time: time of pickup of the order (if available)
delivered_time: time of delivery of the order (if available)
cancelled_time: time of cancellation of order (if the order was cancelled)
cancelled: whether the order was cancelled
rider_id: unique id for each rider
first_mile_distance: road distance from rider’s location to the pickup location
last_mile_distance: road distance from pickup location to the delivery location
allotted_orders: total number of orders allotted to the rider in the 30 days before (not including) order_date
delivered_orders: total number of orders delivered by the rider in the 30 days before (not including) order_date
undelivered_orders: total number of orders allotted to but not delivered by the rider (i.e. cancelled) in the 30 days before (not including) order_date
lifetime_order_count: total number of orders delivered by the rider at any time before order_date
reassigned_order: whether the order was reassigned to this rider
reassignment_method: if the order was reassigned, whether the reassignment was done manually (by the ops team) or automatically
reassignment_reason: a more detailed reason for the reassignment
session_time: total time the rider had been online on order_date before order_time

**New features added**
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


