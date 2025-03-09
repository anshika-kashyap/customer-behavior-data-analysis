# About Datasets

## Overview

The raw dataset consists detailed information about ticket sales and customer behavior at a cinema hall.

- cinema_hall_ticket_sales.csv: The raw dataset.
- cleaned_cinema_hall_ticket_sales.csv: The cleaned dataset.
- cleaned_cinema_hall_ticket_sales_analysis.csv: The cleaned dataset, along with general data analysis.

The interactive Google Workbook, consisting of Google Sheets, Pivot Tables and Charts, can be accessed [here](https://docs.google.com/spreadsheets/d/1AFRHtJ6cEYuu3UAVLJMxcYf-qyxkubRy10_y1VFaOIc/preview).

## Columns Descriptions

The descriptions of the following columns are based on the raw dataset:

- Ticket_ID: A unique alphanumeric identifier for each ticket purchase. The ID consists of a random uppercase letter (A-Z) followed by a 4-digit number.
- Age: The age of the customer who purchased the ticket, ranging between 18 and 60 years.
- Ticket_Price: The price the customer paid for the ticket, typically ranging from $10 to $25. The price varies based on factors like movie time, seat type, or cinema location.
- Movie_Genre: The genre of the movie the customer attended, which can include one of the following: Action, Comedy, Horror, Drama, or Sci-Fi.
- Seat_Type: The type of seat selected by the customer, with three ordinal categories:
  - Standard (Basic seating option)
  - Premium (Enhanced seating with added comfort)
  - VIP (Exclusive seating, offering premium features like extra legroom and priority service)
- Number_of_Person: The number of people accompanying the customer. This can either be:
  - Alone: The customer attended alone.
  - 2–7: The customer attended with a group of 2 to 7 people.
- Purchase_Again: A binary target variable indicating whether the customer is likely to return and purchase another ticket. It has two possible values:
  - Yes: The customer is likely to return for another movie.
  - No: The customer is not likely to return.
 
## Note

Two new columns were added in the [cleaned_cinema_hall_ticket_sales_analysis.csv](https://github.com/anshika-kashyap/customer-behavior-data-analysis/blob/main/datasets/cleaned_cinema_hall_ticket_sales_analysis.csv) called:
  - 'general data analysis': for statistical analysis.
  - 'seat_type_num': for understanding possible correlation between 'seat_type' and 'purchase_again' columns.
