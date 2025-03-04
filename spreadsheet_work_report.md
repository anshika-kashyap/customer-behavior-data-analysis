# Spreadsheet Work Report

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

## Data Analysis

- Created some new cells to check statistics of 'ticket_price' and 'age' columns and correlation of 'age' and 'number of person' columns.
    - Mean and median for 'ticket_price' and 'age' columns were same, indicating our data is balanced and have no outliers.
    - There was no correlation between 'age' and 'number of person' columns.
- As per the cleaned dataset's pivot table:
    - The most brought movie genre was 'Action' and the least was 'Sci-Fi'.
    - The most brought seat type was 'VIP', and the least was 'Premium'.
    - For 'horror' movies, the 'VIP' seats were in demand. For 'drama' movies, 'standard' seats were desired. For 'action' movies, premium were booked most. This data also shows that which genre sold most tickets in each seat category.
    - Highest genre collection was done by 'horror' movies in general, through 'VIP' seats, the sum of 'ticket_prices' is $1,907.60 USD. In general, it was $5,296.52 USD.
    - In total, $25,032.92 business was done overall from all the movie generes and seat types.
- Created a bar graph to check the average age of each genre's viewers.
- Created a pie chart to check the average answer to the question: 'will you purchase another ticket in the future or not?'
- Average age of people watching horror movies is 40, and this was also the eldest average age among all the viewers.
- Most expensive ticket is for 'sci-fi' movie genre and the least is for 'action' movie.
- The average 'ticket_price' is same for 'VIP' and 'premium' seat type, and 0.32 USD less for 'standard' seat type.
- Most seats prefered were 'VIP' and their corresponding average 'ticket_price' is similar to the 'premium' seat type.
    - People prefered better seat type with the same 'ticket_price' level, they prefered relaxing experience.
- As per pivot table, people saying 'No' for 'purchase_again' paid a little more than those people who said 'Yes'. 
    - People who are returning to watch another movie are most probably prefering cheaper tickets or are using some disounts/coupons.
        - This indicates that people using 'standard' seat type are prefering to come, but those which prefer 'premium' or 'VIP' don't prefer to return, as the average 'ticket_price' correspoding to the seat type was same for 'premium' and 'VIP', and lower than them for 'standard'.
- Created a bar graph for customers returning probability corresponding to average ticket price they paid.
- Created a bar graph for average ticket price corresponding to the seat type.
