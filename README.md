# Hotel Booking Dashboard – Power BI Project

## 📌 Project Overview  
This project involves creating a **hotel booking analytics dashboard** using **Power BI**, focusing on key business insights such as **booking trends, revenue performance, customer loyalty, and booking behavior**. The dashboard was built using **a structured dataset, custom design elements, and advanced DAX calculations** to enhance analytical depth.  

## 🎨 Design & Customization Features  
- **Custom Background & Theme:** Designed manually to enhance the dashboard’s aesthetics and provide a professional look.  
- **AI-Generated Logo & Color Palette:** Used for branding and maintaining a consistent visual identity.  

## 📊 Key Business Insights Displayed  
- **Booking Metrics Overview:**  
  - Total Bookings  
  - Cancellation %  
  - Total Revenue  
  - Total Room Nights  
  - Average Room Rate  
- **Daily Stays Trend:** Visualization of how many stays occur per day over time.  
- **Booking Behavior:** Insights into how far in advance customers book their stays.  
- **Weekday vs. Weekend Analysis:** Understanding peak days for bookings.  
- **Loyalty Level Analysis:** Breakdown of guest types (members vs. non-members).  
- **Booking Channel Analysis:** Evaluating the most effective booking sources (Hotel App, Website, Wholesalers, GDS, Phone, etc.).  

![Dashboard Preview](https://github.com/IshaAgarwal1816/PowerBI_Project1_Hotel_Booking/blob/main/Dashboard.png?raw=true)

## ⚡ DAX Calculations Used  
Several **DAX (Data Analysis Expressions) calculations** were implemented to derive meaningful insights from the dataset. Below are the key measures:  

```DAX
-- Total Booking Count
Booking Count = COUNT(bookings[Booking ID])

--  Cancellation Count
Cancellation Count = CALCULATE([Booking Count], bookings[Status] = "Cancelled")

-- Cancellation Percentage
Cancellation Pct = (SUM(bookings[Cancellation Count]) / SUM(bookings[Booking Count])) * 100

-- Total Revenue
Total Revenue = SUM(bookings[Revenue])

-- Total Room Nights
Total Room Nights = SUM(bookings[Number of nights])

-- Average Room Rate
Avg. Room Rate = DIVIDE(SUM(bookings[Room Rate]), SUM(bookings[Booking Count]))

-- Loyal Customer Booking Count
Loyal Customer Booking Count = CALCULATE(COUNT(bookings[Booking ID]), bookings[Loyalty Level] <> "Non-member")

-- Not Loyal Customer Booking Count
Not Loyal Customer Booking Count = CALCULATE(COUNT(bookings[Booking ID]), bookings[Loyalty Level] = "Non-member")

-- Multi-Night Booking Count
Multi-Night Booking Count = CALCULATE(COUNT(bookings[Booking ID]), bookings[Number of nights] > 1)

-- Single Night Booking Count
Single Night Booking Count = CALCULATE(COUNT(bookings[Booking ID]), bookings[Number of nights] = 1)

```

## 📊 Outcome & Learnings  

✅ **Actionable Insights for Hotel Managers**  
The dashboard provides hotel managers with **clear insights** into customer booking trends, revenue drivers, and peak booking periods. This helps in making data-driven decisions to optimize pricing, marketing, and operations.  

✅ **Enhanced Data Interactivity**  
With the use of **custom DAX calculations**, the dashboard allows for **real-time filtering and deep-dive analytics**. Users can interactively explore customer loyalty, booking lead times, and revenue trends to uncover hidden patterns.  

✅ **Professional-Grade Dashboard**  
The project demonstrates a **well-structured, visually appealing, and interactive dashboard** with:  
- **AI-generated branding elements** for a polished look.  
- **Custom-designed background** to ensure a premium user experience.  
- **Segmented visuals and slicers** for effortless data exploration.  

This project is a **real-world business application** that showcases strong **Power BI skills, data modeling, and storytelling**—making it a valuable portfolio piece for analytics and product management roles.  

