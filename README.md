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
+ Addressing outliers in numeric variables
+ Modifying datatype and encoding categorical variables, with encoded values were shown in the below table

| **Feature** | **Original value** | **Encoded value**|
| :---:   | :---: | :---: |
| Gender | Female | 0 |
| Gender | Male | 1 |
| Customer Type | First-time | 0 |
| Customer Type | Returning | 1 |
| Type of Travel | Personal | 0 |
| Type of Travel | Business | 0 |
| Class | Economy | 0 |
| Class | Economy Plus | 1 |
| Class | Business | 2 |

+ and lastly, Feature selection

The final dataset was employed to perform EDA and analyze.

## 1. Average score of each criteria

The below table showed the average score for each flight's feature in ascending order. On average, In-flight Wifi service and Ease of Online Booking were the two worst features with the lowest average score of 2.73 and 2.76 respectively, compared to other features. It can be because In-flight Wifi quality has lower bandwidth and speed, due to the limitations of the technology and the distance involved, which can result in poor performance, slow loading, and disconnection. On the contrary, In-flight Service and Baggage Handling gained the highest average scores of over 3.6. However, in general, the scores of these flight's criterion were not high because their scores only ranged from 2.7 to 3.6.

| Flight's feature | Average score    |
| :---:   | :---: |
| $\color{red}{In-flight\ Wifi\ Service}$ | $\color{red}{2.727}$   |
| $\color{red}{Ease\ of\ Online\ Booking}$ | $\color{red}{2.757}$|
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

## 2. Relationship between passenger's information features and the overall Satisfaction
According to the below bar plots, Gender and Customer type may not have strong affect on the satisfaction level since the difference between the quantity of dissatified and satisfied passengers were not huge between their classes.

In terms of Travel Type, it can be seen that to personal-purpose trips, the majority of passengers dissatisfied or neutral with their airplanes, which was significantly higher than the number of satisfied passengers. On the contrary, business-purpose trips witnessed the opposite situation since more passengers were satisfied.

To Class variable, the quantity of satisfied passengers using Business class was about double the figure for the remaining group. However, to Economy and Economy plus classes, majority of passengers were dissatisfied or neutral, especially to Economy class, the number of dissatisfied or neutral passengers were over 4 times the figure for satisfied passengers.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/passenger_info_satisfaction.png">
</p>

## 3. Relationship between numeric variables and the overall Satisfaction
According to the below boxplots, Arrival Delay variable may not bring huge effect on satisfaction level since the average arrival delay in both satisfied and disatisfied groups were pretty similar.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/numerical_var_satisfaction.png">
</p>

There is a difference in the average age between both groups, however, this difference is pretty small, and their IQR range were overlapped with each other, which may not indicate a strong relationship between age and satisfaction level.

It can be seen that the average flight distance in Satisfied group were higher than the figure for the remaining group. In addition, the IQR range of flight distance in Satified group is much further to the top of the boxplot, which means that Satisfied group contains more longer flights than the Dissatisfied and neutral group.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/business_flightdistance_satisfaction.png">
</p>

According to the above plots, passengers with business-purpose trips tended to travel longer routes, which was shown by the higher average flight distance in the first left boxplot. Hence, passengers may prefer to buy Business class tickets, especially when their flights were much longer, which can be seen in the second and the third plot. In the third boxplot, the quantity of Business class in Business travel type was doubled the quantity of Economy, and over 10 times higher than the number of Economy Plus class. In addition, while the average flight distance of Economy and Economy Plus in Business travel type were pretty similar to the figure for personal-purpose trips, the average flight distance of Business class was much greater, as presented in the second boxplot.

In addition, since Business class has more benefits than other classes such as seat comfort, premium meals and drinks, priority check-in and boarding, complimentary amenity kits, legroom service,... passengers travelled with Business class tended to give higher scores for most flight's features such as Check-in Service, Online Boarding, On-board Service, Seat Comfort, Leg Room Service, Cleanliness, In-flight Service, and In-flight Entertainment, as shown in the below boxplots, and more likely to be satified with their flights than passengers travelling with Economy class.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/business_satisfaction.png">
</p>

This also can explain for the situation observed above, which showed that the higher quantity of satisfied passengers gathered in Business group of Travel Type, greater values of Flight Distance, and Business class of Class variable.

## 4. Relationship between each criteria and the overall Satisfaction
Among all variables related to passenger evaluation of flight's features, factors might not have strong relationship with satisfaction level were Departure and Arrival Time Convenience, Ease of Online Booking, Gate Location, In-flight service, Baggage Handling because their avarage value between two satisfaction levels were pretty the same, as shown in below plots.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/norelationship_var_satisfaction.png">
</p>

To other variables, generally, when passengers give high score for these factors, they tend to be satisfied with their flight. It was because the average score of most factors in Satisfied group were higher than the figures for Dissatisfied or Neutral group. For example, Online Boarding factor can have a stronger positive relationship with satisfaction level since more than 75% of satisfied passengers give a score of 4 or above to this critera, while 75% dissatisfied or neutral passengers give only a score of 3 or below. Hence, if passengers give a score of 4 or above to this Online Boarding factor, it is more likely that they can be classified in Satisfied group. Similarly, it also can be seen that 75% passengers in Satisfied group give a score of 4 or above to the In-flight Entertainment factor, while the figures for the remaining group was only about 25%. Therefore, with a score of 4 or above, passengers are more likely to be satisfied with their flights.

<p align="center" width="100%">
    <img width="100%" src="https://github.com/Tien-le98/DA_Project_Airlines-Satisfaction/blob/main/relationship_var_satisfaction.png">
</p>

## CONCLUSION

After performing EDA on this Airline Quality Ratings dataset, there are several main points as following:
+ Outliers existing in many numerical variables such as Flight Distance and Arrival Delay, however, these outliers were still in the valid range, and there are no specific reasons to remove them. Hence, these outliers were still kept in the dataset.
+ In general, when passengers give high score for flight's features, they tend to be satisfied with their flights. It was because the average score of most factors in Satisfied group were higher than the figures for Dissatisfied or Neutral group.
+ To business-purpose trips, passengers tended to travel longer routes than personal-purpuse trips. Therefore, they prefer to use Business class, especially when their flights were much longer. Since Business class has more advantages than other classes such as priority check-in and boarding, seat comfort, legroom,..., passengers tend to give higher scores for these flight's features, and hence they are more likely to be satisfied with their flights.
+ In comparison with other flight's features, In-flight Wifi service and Ease of Online Booking were the two worst features with the average score of only 2.73 and 2.76 respectively, evaluated by 130000 passengers. It can be because In-flight Wifi quality has lower bandwidth and speed, due to the limitations of the technology and the distance involved, which can result in poor performance, slow loading, and disconnection.
+ Most of other features gained average scores only between about 3 and 3.6. This means that all these criterion should improved in the future. However, several features, having stronger relationship with satisfaction level, should be paid more attention, which are Check-in Service, Online Boarding, On-board Service, Seat Comfort, Leg Room Service, Cleanliness, Food and Drink, In-flight Wifi Service, In-flight Entertainment.
+ There are several ways to enhance these criterion. For example, the airline can implement more flexible seating arrangements to improve seat comfort, invest in machines which can assist passengers with online boarding and online check-in more quickly and smoothly, redesign in-flight menu to meet customers' preferences, needs, and expectations, and research for new and more cost-effective Wifi solutions to increase Wifi quality on planes.
