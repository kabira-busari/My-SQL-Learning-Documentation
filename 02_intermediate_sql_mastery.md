## Intermediate SQL (Course 2)
This is the documentation for the "Intermediate SQL" course I completed as part of the [Associate Data Analyst in SQL Career Track](https://app.datacamp.com/learn/career-tracks/associate-data-analyst-in-sql) on DataCamp.

### Course Overview
In this course, I built upon the foundational SQL concepts learned in the introductory course. I explored more advanced techniques for filtering, sorting, grouping data, and working with missing values. These skills allow for deeper analysis and more refined querying of large datasets.

### Key Concepts Covered:
#### 1. COUNT() and LIMIT:
- COUNT() allows for counting records, both overall and based on distinct values.
- LIMIT helps in controlling how many results are returned. Example:
```SQL
SELECT COUNT(*) 
FROM reviews;
```
This query counts the total number of reviews in the database.

#### 2. Filtering Records with WHERE Clause:
I learned how to filter records based on conditions, using comparison operators (=, <, >, etc.) and string matching.
I also explored the logical operators AND, OR, and BETWEEN to combine multiple filtering criteria.
Example:
```SQL
SELECT title, release_year 
FROM films 
WHERE release_year BETWEEN 1994 AND 2000;
```
This query retrieves all films released between 1994 and 2000.

#### 3. Handling Missing Values:
I learned to work with missing data using IS NULL and IS NOT NULL.
```SQL
SELECT title 
FROM films 
WHERE budget IS NULL;
```
This query retrieves all films where the budget information is missing.

#### 4. Aggregate Functions (AVG, SUM, MIN, MAX, COUNT):
Aggregate functions allow for summarizing data. I learned how to calculate averages, sums, minimums, maximums, and counts.
Example:
```SQL
SELECT AVG(budget) AS avg_budget 
FROM films 
WHERE release_year > 2010;
```
This query calculates the average budget of films released after 2010.

#### 5. Sorting Data:
ORDER BY was used to sort query results, either in ascending or descending order. Sorting by multiple fields is possible by separating them with commas.
Example:
```SQL
SELECT title, release_year 
FROM films 
ORDER BY release_year DESC, title;
```
This query sorts films by release year in descending order, then alphabetically by title.

#### 6. Grouping and Filtering Grouped Data:
GROUP BY helped me group records by a specific field, and I used HAVING to filter the results of grouped data.
Example:
```SQL
SELECT release_year, COUNT(title) AS films_per_year 
FROM films 
GROUP BY release_year 
HAVING COUNT(title) > 5;
```
This query shows only the years where more than five films were released.

### Hands-on Projects
As part of this course, I applied the concepts to a Cinema database, which contains tables like films, reviews, people, and roles. You can check out the queries and analysis I performed using these datasets in my DataCamp DataLab.

🔗 Check my detailed analysis here: [SQL Learning Journal: Associate Data Analyst Track (Course 2 - Intermediate SQL)](https://www.datacamp.com/datalab/w/93888de5-f27f-4e5d-9b0d-f0882ea9fb8d/edit)

### How to Use This Repository
This repository contains the structured learning of my SQL journey, including:
- Detailed explanations of key concepts.
- Sample queries from the Cinema database.
- Real-world applications to show how SQL can be applied in data analysis scenarios.
Feel free to explore each course folder for an in-depth look at my SQL learning process.


