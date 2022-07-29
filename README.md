# EDA-CAPSTONE-PROJECT

# ***Hotel-Booking-Analysis***

The project contains the real world data record of hotel bookings of a city and a resort hotel containing details like bookings, cancellations, guest details etc. from 2015 to 2017. In this project we are going to analyze Hotel Booking Data in order to find out valuable insights and give suggestions to increase revenue of hotels.


**Programming Language** : Python


**Libraries used** : Pandas, Numpy, Matplotlib, Seaborn


**NoteBook** : Google Colab


**Dataset Source** : Provided by Almabetter themself.


## Objective :--
We are provided with a hotel bookings dataset.

The main purpose of this study is to perform EDA on the given dataset and draw useful conclusions about the trends in hotel bookings and how factors that control hotel bookings influence each other.


## Dataset :--
We are given a hotel bookings dataset. This dataset contains booking information for a city hotel and a resort hotel. It contains the following features.

  - hotel: Name of hotel ( City or Resort)
  - is_canceled: Whether the booking is canceled or not (0 for no canceled and 1 for canceled)
  - lead_time: time (in days) between booking transaction and actual arrival.
  - arrival_date_year: Year of arrival
  - arrival_date_month: month of arrival
  - arrival_date_week_number: week number of arrival date.
  - arrival_date_day_of_month: Day of month of arrival date
  - stays_in_weekend_nights: No. of weekend nights spent in a hotel
  - stays_in_week_nights: No. of weeknights spent in a hotel
  - adults: No. of adults in single booking record.
  - children: No. of children in single booking record.
  - babies: No. of babies in single booking record. 
  - meal: Type of meal chosen 
  - country: Country of origin of customers (as mentioned by them)
  - market_segment: What segment via booking was made and for what purpose.
  - distribution_channel: Via which medium booking was made.
  - is_repeated_guest: Whether the customer has made any booking before(0 for No and 1 for Yes)
  - previous_cancellations: No. of previous canceled bookings.
  - previous_bookings_not_canceled: No. of previous non-canceled bookings.
  - reserved_room_type: Room type reserved by a customer.
  - assigned_room_type: Room type assigned to the customer.
  - booking_changes: No. of booking changes done by customers
  - deposit_type: Type of deposit at the time of making a booking (No deposit/ Refundable/ No refund)
  - agent: Id of agent for booking
  - company: Id of the company making a booking
  - days_in_waiting_list: No. of days on waiting list.
  - customer_type: Type of customer(Transient, Group, etc.)
  - adr: Average Daily rate.
  - required_car_parking_spaces: No. of car parking asked in booking
  - total_of_special_requests: total no. of special request.
  - reservation_status: Whether a customer has checked out or canceled,or not showed 
  - reservation_status_date: Date of making reservation status.


  - Total number of rows in data: 119390
  - Total number of columns: 32


## Data Cleaning :--

### (1) Handling null values
  - Null values in columns `company` and `agent` were replaced by 0.  
  - Null values in column `country` were replaced by 'others'.
  - Null values in column `children` were replaced by the mean of the column.


### (2) Converting columns to appropriate data types
  - Changed data type of `children`, `company`, `agent` to int type.


### (3) Removing Duplicate rows
  - All duplicate rows were dropped.


### (4) Renaming the columns
  - The `adr` column was renamed for better understanding to `average_daily_rate`


### (4) Removing outliers
  - One outlier was found in the `average_daily_rate` column. Dropping them.


### (5) Creating new columns
  - Creating new column `Total_stay` by adding `stays_in_weekend_nights`+`stays_in_week_nights`.
  - Creating new column `Total_members` by adding `adults`+`children`+`babies`.


## Exploratory Data Analysis :--
Performed EDA and tried answering the following questions:

  - Which hotel has more no of bookings and What is the  percentage of bookings in each hotel ?
  - Hotel Wise Bookings based on Month and year, also What is the trend of bookings within a month ?
  - Which meal type is the  most preffered meal of customers ?
  - Country Wise - Number of Bookings ?
  - Which agent is making maximum Bookings ?
  - Which room type is in most demand and which room type generates the  highest average daily rate?
  - How long do people stay at the hotels?
  - What is preferred stay length in each hotel based on weekday nights and weekend nights ?
  - Which Booking is preffered with the deposit type?
  - Cancellation rates in both the hotels also arival year and  lead time?
  - What is the Average daily rate month wise also which are the most busy months??
  - What is the Average daily rate with respect to per person?
  - Is thier any Special request given by the customer to hotels?
  - Which channel is mostly used for the booking of hotels? 
  - Chances that its customer will return for another stay?
  - Which types of customers mostly make bookings?
  - How many customers are most likely to require a parking space?
 

*Mainly performed using Matplotlib and Seaborn library and the following graph and plots had been used:*
 
  - **Bar Plot.**
 
  - **Scatter Plot.**
 
  - **Pie Chart.**
 
  - **Line Plot.**
  
  - **Heatmap.**
 
  - **Box Plot.**
     
     
## Analysis :--
**Univariate Analysis:**
*Performed univariate analysis and made following conclusions:*
  
  - Agent no. 9 has made most no. of bookings.
  
  - Most demanded room type is A, but better adr generating rooms H, G and C. Hotels should increase the no. of room types A and H to maximise revenue.
  
  -  Most popular meal type is BB(Bed and Breakfast).
  
  - Around 60% bookings are for City hotel and 40% bookings are for Resort hotel, therefore City Hotel is busier than Resort hotel.
  
  - Guests use different channels for making bookings out of which most preferred way is TA/TO.
  
  - July- August are the most busier and profitable months for both of hotels. 
  
  - Most of the guests came from european countries, with highest number of guests from Portugal.
  
  - Most common stay length is less than 4 days and generally people prefer City hotel for short stay, but for long stays, Resort Hotel is preferred.
 
 
**Bivariate Analysis :**
*We tried to answer following questions*

  - Overall adr of City hotel is slightly higher than Resort hotel and no. of bookings of City hotel is also higher than Resort hotel. Hence, City hotel is makes more revenue.
  
  - City hotel has slightly higher median lead time. Also median lead time is significantly higher for both hotels, this means customers generally plan their hotel   visits way early.
  
  - Almost 30 % of City Hotel bookings got canceled.
  
  - Both hotels have very small percentage that customer will repeat, but Resort hotel has slightly higher repeat % than City Hotel.
  
  - TA/TO is mostly used for planning Hotel visits well ahead of time. 
  
  - While booking via TA/TO one may have to wait a little longer to confirm booking of rooms.
  
  - GDS channel brings higher revenue generating deals for City hotel, in contrast to that most bookings come via TA/TO. City Hotel can work to increase outreach on GDS channels to get more higher revenue generating deals.
  
  - TA/TO has highest booking cancellation %. Therefore, a booking via TA/TO is 30% likely to get cancelled.
  
  - Longer lead time has no affect on cancellation of bookings.
  
  - Not getting same room as demanded is not the case of cancellation of rooms. A significant percentage of bookings are not cancelled even after getting different room as demanded.
  
  - Not getting same room do affects the adr, people who didn't got same room have paid a little lower adr. 
  
  - Arrivals in hotels increases at weekends and also the avg adr tends to go up as month ends. 


## Conclusion :--

We used the dataset that contains data about **hotel bookings.**

We ***cleaned and preprocessed*** the data and then we performed the ***exploratory data analysis*** to extract infromation from the data.

After analysing the dataset we can conclude that :--  

 - More than ***61%*** of the population booked the **city hotel** for their stay.

 - Out of three years ***2016*** is the **busiest** for hotels.

 - Most no of the bookings are made in the middle part of the year(specifically, ***July and August***) decreasing toward the start and end of the year.

 - The majority of guests come from ***western europe countries*** with ***Portugal*** being the leader.

 - Given that we only have ***4%*** repeated guests. We should target our advertisement on guests to increase returning rate.

 - ***80%*** distribution_channel is of **TA/TO**

 - Most common stay length is **less than or equal to 4 days** and generally people prefer ***City hotel*** for **short stay**, but for ***longer stays***, **Resort Hotel** is preferred.

 - ***Couple(or 2 adults)*** is the most polpular accomodation type. So hotels can make arrangement plan accordingly.

 - Guests use different channels for making bookings out of which most preferred way is **TA/TO**

 - For customers, generally the longer stays (more than 15 days) can result in better deals in terms of **low** average daily rate.


## Challenges

 - Lot of null values were present in the dataset.
 - Data type of some Data was in wrong format.
 - Lot of duplicate data.
 - Which visualization techniques to use was a challenge?
