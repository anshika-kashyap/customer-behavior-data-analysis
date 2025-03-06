# Spreadsheet Work

## Exploratory Data Analysis (EDA)

- As per the column basis description of the dataset:
    - Raw dataset had:
        - 1440 rows
        - 7 columns
    - Raw dataset had columns divided into following datatypes categories:
        - String - 4
        - Integer - 1
        - Boolean - 1
        - Other - 1
    - No null values in the raw dataset.
    - 1436 unique values in the 'Ticket_ID' column, suggesting that there were 1436 unique tickets out of 1440 tickets. This means that there were 4 possible duplicates in the dataset.
    - 5 unique movie genre's, 3 unique seat-types, 7 unique values in 'Number_of_Person' column.
    - 707 'True' values and 733 'False' values in the 'Purchase_Again' column.
 
## Data Cleaning

  - Duplicated the raw dataset, and named the duplicate 'Cleaned Dataset'. We will focus on cleaning the dataset in this duplicated version.
- Trimmed any possible whitespaces in the whole dataset.
    - There was no whitespace in the dataset.
- Turned all the headers into lowercase.
- Left aligned all the data.
- Autofitted all the columns.
- Colored the header and froze it.
- Colored the data.
- Turned 'age' and 'ticket_price' columns into 'number' datatype.
    - NOTE: The 'ticket_price' column have price written in US Dollars.
- Looked for duplicate rows.
    - There were 4 duplicate tickets in the 'ticket_id' column, but no duplicate rows. The possible causes for this could be:
        - System error
        - Typo
        - Multiple people used same tickets again and again, a management error
    - Checked how much the duplicates differ from the original by checking the other column values, by filtering and conditionally formatting the dataset.
    - Duplicates differ a lot, they were typo's/system error.
    - Removed the duplicates in our case as:
        - They were typo's/system error.
        - There was enough data to analyze, we can omit the data which don't resonate with the original data.
        - Deleted the conditional formatting and the duplicates [Google Sheets: 4 duplicate rows found and removed. 1436 unique rows remain.].
- Sorted the data into ascending order by 'ticket_id'. 
- Checked for outliers in 'ticket_price' and 'age' columns using formula.
    - No outliers found.
- Turned 'Alone' to '0' in 'number_of_person' column.
- Changed the datatype of 'number_of_person' column to 'number'.
- Changed 'No' to '0' and 'Yes' to '1' in the 'purchase_again' column, for easy analysis.
- Changed the datatype of 'purchase_again' column to 'number'.

## Data Analysis

- Duplicated the cleaned dataset and named the duplicate 'Cleaned Dataset - Analysis' to create a new column for general analysis.
- To analyze why some customers rejected the idea of purchasing another movie tickets in the future and some agreed, we will focus on 'purchase_again' column and it's relation with other columns.
- Checked the number of times 1 (Yes) and 0 (No) occured in the dataset.
    - 1 occured 705 times and 0 occured 731 times.
    - Most of the customers rejected the idea of purchasing another movie tickets in the future.
- Which people rejected and which accepted the offer?:
    - Average number of people accompanied by customers was same for both the parties.
    - Average age of customers who said 'No' and who said 'Yes' was same.
    - Average ticket price paid by customers who said 'No' paid a little more than those people who said 'Yes' to 'purchase_again'.
    - The people who watched 'drama' and 'horror' genre, said 'Yes' most of the time, and others said 'No' in general.
    - Most people who opted for 'VIP' and 'Premium' seat type said 'No' and those who opted for 'Standard' seat type said 'Yes'.
- Those who paid more for tickets, those who watched 'comedy', 'action', 'sci-fi' and those who opted for 'VIP' and 'Premium' seats, said 'No' to purchasing another movie tickets again.
- Created a pivot table to summarise data well.
- As per the pivot table and bar graph created thorugh it:
    - Most of the seats that were opted in the 'action', 'sci-fi' and 'comedy' genres were 'VIP' and 'Premium'.
    - In horror, 'VIP' seats and in drama, 'Standard' seats were the focus, at the same time, their tickets costed less.
    - People paid more for the seats and less for the movie tickets in the case of horror genre, and less for both in the case of drama genre.
- A trend can be seen here: People who paid more and for the theatre experience, by watching most expensive movies, opting for most expensive seats, said 'No' for purchasing another movie tickets again; and people who paid comparatively less and watched movies for movie experience/stroytelling, by watching horror and drama movie for stories and opting for 'standard' seats or 'less ticket price and more seat price' combination, said 'Yes' for purchasing another movie tickets again.
- Created a chart using pivot table 2 and created a bar graph using it.
- Created a bar graph using cleaned data to see percentage distribution of seat types.
- The bar graph of pivot table 2 cleary shows that those who said 'No' paid more for their seats as they had opted for 'Premium' and 'VIP' seats, whereas 'Standard' seats haven't costed the 'Yes' answered custoemrs much.
- Created pivot table 3 and a bar grpah out of it to show the average ticket price as per the movie genre.
- Most opted seat type was 'VIP', and 'Premium' was opted by almost the same amount of people who opted for 'Standard', which made majority of the people to say 'No' for another movie, and second opted option in general was 'Standard' which was cost effective and hence, made the rest of the people say 'Yes'.
- Found out the possible correlations. Created a new column 'seat_type_num' which represents each 'seat_type' as:
    - Standard - 0
    - VIP - 1
    - Premium - 2
        - There was no correlation between any of the numerical columns, and between the 'seat_type' and the 'purchase_again' column.
