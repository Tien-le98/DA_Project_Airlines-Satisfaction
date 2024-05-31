# DA_Project_Airlines-Satisfaction
_Author: Clara Le_

_Date: 31/5/2024_

---
This project employed Airline Quality Ratings dataset to determine the relationship between relevant factors and Passengers' Satisfaction level of their flights. This satisfaction was measured by nearly 130000 airline passengers. Relevant factors can be classified into 2 main groups, which are Passenger information and Flight features. 
1. Group **Passenger information** includes features related to each passenger:
+ ID: Passenger ID
+ Gender: Passenger gender (Male, Female)
+ Age: Passenger age
+ Customer Type: Customer type of passenger (Returning, First-time)
+ Type of Travel: Purpose of the flight of passenger (Business, Personal)
+ Class: Travel class in the plane of passenger (Business, Economy, Economy Plus)
2. Group **Flight** features comprises of each flight's characteristics, and **passenger's evaluation** of each flight's features, which ranges from 0 to 5.
+ Flight Distance: The distance between the departing place and the destination of each flight
+ Departure Delay: Minutes delayed when passengers depart
+ Arrival Delay: Minutes delayed when passengers arrive
+ Departure and Arrival Time Convenience: Passenger evaluation of the convenience of departure and arrival times Ease of Online Booking: Passenger evaluation of the ease of online booking
+ Check-in Service: Passenger evaluation of the ease of check-in service
+ Online Boarding: Passenger evaluation of the convenience of online boarding
+ Gate Location: Passenger evaluation of the gate location estimation
+ On-board Service: Passenger evaluation of the service on board
+ Seat Comfort: Passenger evaluation of their seat's comfort
+ Leg Room Service: Passenger evaluation of their legroom (Legroom is the amount of space between passenger's seat and the seat in front of them on a plane)
+ Cleanliness: Passenger evaluation of the aircraft's cleanliness
+ Food and Drink: Passenger evaluation of the quality of food and drinks
+ In-flight Service: Passenger evaluation of the level of service in flight
+ In-flight Wifi Service: Passenger evaluation of the wifi quality in flight
+ In-flight Entertainment: Passenger evaluation of the in-flight entertainment
+ Baggage Handling: Passenger evaluation of baggle handling

These above factors were then used to measure the overall passenger's satisfaction level, which was presented in the target variable (**Satisfaction** : Neutral or Dissatisfied, Satisfied).

After check the summary statistics, as well as features' distribution, several major data cleaning steps were implemented, including:
+ Handling missing values in Arrival Delay variable
+ Modifying datatype and encoding categorical variables
+ Addressing outliers in numeric variables
+ Feature selection

The final dataset was employed to perform EDA and analyze.

## 1. Average score of each criteria

The below table showed the average score for each flight's feature in ascending order. On average, In-flight Wifi service and Ease of Online Booking were the two worst features with the lowest average score of 2.73 and 2.76 respectively, compared to other features. On the contrary, In-flight Service and Baggage Handling gained the highest average scores of over 3.6. However, in general, the scores of these flight's criterion were not high because their scores only ranged from 2.7 to 3.6.

| Flight's feature | Average score    |
| :---:   | :---: |
| $\color{green}{In-flight\ Wifi\ Service}$ | 2.727   |
| Ease of Online Booking | 2.757   |
| Gate Location	| 2.977|
|	Departure and Arrival Time Convenience|	3.058|
|	Food and Drink |	3.205|
|	Online Boarding	| 3.253|
|	Cleanliness	| 3.286|
|	Check-in Service |	3.306|
|	Leg Room Service	| 3.351|
|	In-flight Entertainment	| 3.358|
|	On-board Service	| 3.383|
|	Seat Comfort	| 3.441|
|	Baggage Handling | 3.632|
|	In-flight Service	| 3.642|
