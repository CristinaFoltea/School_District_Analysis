# School_District_Analysis

Math and reading scores analysis. 
 - Calculating the average score and percentage of passing students based on different criteria:
    - all schools and district,
    - per school,
    - per school size,
    - per school budget,
    - per school, per grade

## Resources
  - Data sources: students_complete.csv, schools_somplete.csv

## Challenge

How is the district summary affected?
  - The average scores for math and reading remained relatively constant. Probably due to the fact that .mean() function in pandas excludes the nan values by default.
  - The number of students passing math and reading decreased as a result of missing data.
  - The percentage of passing students for both math and reading decreased since the students with missing records are treated as students that didn't pass the tests.
  - If we update the calculation for the percentage of passing students to use the number of students with data instead of the total amount of students we get a percentage similar the one before we removed the data.

How is the school summary affected?
  - Similar to the district summary the average score for didn't change significantly but the percentage of math, reading and overall passing decreased significantly since the total number of students is used in calculating those percentage.

How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance, relative to the other schools?
 - The missing data significantly influence the percentage of students at the Thomas High School that passed math and reading. In the performance top, the school went from the 2nd place to the 8th place.

How does replacing the ninth-grade scores affect the Math and Reading Scores by Grade, Scores by School Spending, Scores by School Size, and Scores by School Type? 
  - Math and Reading Scores by Grade - Since we did the analysis per grade per school and all the data for the Thomas High School 9th grade is missing the analysis shows that in the resulting data frames as "NAN". If we were analyzing the data based on grades for all schools we would see the same results as with the previous analysis where the average score stays relatively constant but the percentage of passing students for the 9th grade would decrease.
  - Scores by School Spending - The $630-644 bin sufers a significant drop in passing percentage
  - Scores by School Size - Medium school size have a lower passing percentage as result of the missing data
  - Scores by School Type - Charter schools have a lower passing percentage as result of the missing data
