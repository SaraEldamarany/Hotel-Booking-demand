# Hotel Booking Demand Analysis

This project was delivered as a freelance task through the Khamsat platform.
The objective was to design a professional and interactive Power BI report based on hotel booking data, offering valuable business insights into customer behavior, reservations, cancellations, and international reach.



The report is divided into two main summary pages with interactive filters and navigation buttons, ensuring a smooth and dynamic user experience.
## Navigation Buttons
- **Page 1**: Reservation Overview
- **Page 2**: Cancellation Insights


## Filters
Professional titles for the slicers (filters) used:
- **Customer Type**: Filter data based on the type of customer.
- **Deposit Type**: Analyze reservations by deposit types.
- **Arrival Year**: Explore data year-over-year.
- **Cancellation Status**: View bookings by their cancellation state.

---

## Visualizations and Descriptions

### 1. Guest Composition Overview (Pie Chart)
Displays the distribution of adults, children, and babies among the reservations. This chart helps understand the primary demographics that hotels are catering to.

### 2. Daily Cancellation Trends (Line Chart)
Shows the number of cancellations per day of the month. This trend identifies which days experience the highest cancellation rates, providing insights for operational planning.

### 3. Customer Special Requests (Stacked Bar Chart)
Illustrates the total special requests made by different customer types. It highlights customer engagement and special needs across segments.

### 4. Reservations by Country (Map)
A map visual showing the volume of reservations by country, with bubble sizes representing the count. Useful to understand the geographical spread of the customer base.

### 5. Average Waiting Time by Hotel (Stacked Bar Chart)
Visualizes the average days customers spend on the waiting list for each hotel type. It offers insights into reservation delays and hotel capacity.

### 6. Monthly Cancellation Trends (Line Chart)
Tracks the number of cancellations by month of arrival date. This helps in identifying seasonal patterns affecting booking stability.

### 7. Reservation Volume by Month (Line Chart)
Displays the monthly trend of reservations, providing a view into peak seasons and low seasons for the hotels.

### 8. Reservation Share by Hotel Type (Donut Chart)
Compares the proportion of reservations between different hotel types. This visual helps stakeholders understand hotel performance.

### 9. Repeat Guest Analysis (Clustered Column Chart)
Counts the number of repeated guests by customer type, showing loyalty patterns among different groups.

### 10. Country-Wise Reservation Table (Table)
Presents a table with country names, cancellation rates, arrival years, and agent numbers. It gives a clear, detailed overview of international booking behaviors and agent involvement.

---

## Measures and Calculations

- **Cancellation Status**: Created as a calculated column to identify cancelled vs. non-cancelled bookings.
- **Reservation Count**: 
```DAX
Reservation Count = COUNT('Hotel booking Demand (1)'[Cancellation Status])
```
Calculated by counting reservations where `Cancellation Status` = "Not Cancelled".

- **Average of Waiting**:
```DAX
Average of Waiting = AVERAGE('Hotel booking Demand (1)'[days_in_waiting_list])
```
Calculates the average days a booking stays on the waiting list.

---

## Chart Construction Tips

- **Line and Stacked Column Chart for Top 7 Countries**:
    1. Create a measure to calculate reservation counts.
    2. Use "Top N" filter on Country based on reservation count.
    3. Add `Arrival Date Year` as column series for better year-over-year comparison.
    4. X-axis: Countries | Y-axis: Reservation count.

---

## Final Notes

This project aims to provide hotel management and marketing teams with actionable insights to optimize booking strategies, understand customer behavior, and enhance overall service delivery.

---
