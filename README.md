**Ola Rides Data Analysis - Power BI Dashboard Documentation**

**1. Introduction**

This document provides an in-depth explanation of the Power BI dashboard created for analyzing Ola ride data. The dashboard focuses on key metrics such as revenue, cancellations, and ratings, utilizing DAX calculations to generate insights.

**2. Dashboard Overview**

The Power BI dashboard consists of multiple sections:

Overall - Provides an overview of ride bookings and key metrics.

Vehicle Type - Analysis of different vehicle categories.

Revenue - Revenue insights by payment method and ride distance.

Cancellation - Breakdown of canceled rides by customers and drivers.

Ratings - Driver and customer ratings for different vehicle types.

**2.1 Screenshots of the Dashboard**

Below are the visual representations of different sections of the dashboard:

Revenue Dashboard
![image](https://github.com/user-attachments/assets/0039344e-6cc7-4f2f-9107-d7251d2b7253)

Cancellation Dashboard
![image](https://github.com/user-attachments/assets/76dd7d12-32a7-4776-92d7-7a2c42e27cab)

Ratings Dashboard
![image](https://github.com/user-attachments/assets/09546d44-cd89-4a7f-a677-f627fd07d50d)


**3. Data and Transformation Process**

The dataset used for this dashboard includes ride details such as booking status, payment method, ride distance, and customer ratings. Data cleaning and transformation were performed using Power Query to ensure accuracy.

**4. Key DAX Formulas**

**4.1 Total Bookings**

TotalBookings = COUNTROWS(July)

This formula counts the total number of ride bookings in the dataset.

**4.2 Canceled Bookings**

CanceledBookings = CALCULATE(COUNTROWS(July), July[Booking_Status] IN {"Canceled by Driver","Canceled by Customer"})

This formula calculates the number of rides canceled by either drivers or customers.

**4.3 Cancellation Rate**

CanceledBookingPercentage = DIVIDE([CanceledBookings], [TotalBookings], 0)

This formula determines the percentage of canceled bookings.

**5. Insights and Findings**

**5.1 Revenue Analysis**

Cash payments contribute the highest revenue, followed by UPI.

Credit and debit card payments are significantly lower in volume.

Ride distances are consistently distributed throughout the month.

**5.2 Cancellation Insights**

28.08% of total bookings were canceled.

The primary reasons for customer cancellations include drivers not moving towards pickup locations and changes in travel plans.

Drivers most frequently cancel due to personal and vehicle-related issues.

**5.3 Ratings Analysis**

Customer ratings are consistently higher than driver ratings.

Prime Sedan and SUVs receive the highest ratings, while bikes and e-bikes have slightly lower ratings.

**6. Recommendations**

Improve Digital Payments: Encourage more UPI and card payments to reduce cash dependency.

Reduce Cancellation Rate: Implement driver incentives to ensure pickups and minimize cancellations.

Enhance Customer Experience: Address customer grievances related to driver behavior and vehicle conditions.

Improve Driver Ratings: Provide training for drivers to enhance customer service quality.

**7. Conclusion**

This Power BI dashboard provides a comprehensive view of Ola ride performance, highlighting revenue trends, cancellation behavior, and customer satisfaction. The insights derived can help optimize operations and improve overall service efficiency.

