# School_District_Analysis
## Overview of the school district analysis
This project analyzes data from a variety of sources and a variety of formats from a city school district. Our analysis will prepare all standardized test data for anaysis, reporting and presentation to provide insights about performance trends and patterns. These insights are used to inform discussions and strategic decisions at the school and dsitrict level about school budget and priorities. This analysis provided shines a light on student funding as well as students standardized test scores.

Further to our analysis, we are investigating eveidence of academic dishonesty in he students data provide in the students_complete.csv file; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards.  Our analysis will thus aim to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. We would then repeat the analysis the school district analysis and show the changes affected the overall analysis.

At the end of our analysis we will be able to provide insights on the following questions:
  - How is the district summary affected?
  - How is the school summary affected?
  - How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?

How does replacing the ninth-grade scores affect the following:
  - Math and reading scores by grade
  - Scores by school spending
  - Scores by school size
  - Scores by school type
### Control Flow
1. Inspect the schools_complete.csv and students_complete.csv to determine number of rows and columns, datatypes, and if the data readable, or if it needs to be converted in some way?
2. Determine our analysis objectives
3. Load and read our csv files
4. Using the count(), isnull(), notnull() methods, find and handle missing values if they are present
5. Determine datatypes to dertermine if conversion is required for the purpose of calculation
6. using the tolist(), split(), and set() methods get the unique incorrect student names and isolate the prefixes and suffixes
7. using the replace() method, fix the Students2019 Names
8. Merge the two dataframes and get number of students, number of schools, Total Budget, Score Averages, and Passing Percentages
9. Create a District Summary DataFrame
10. Format and Reorder the District Summary DataFrame Columns
11. To get a similar summary per school, Set the Index to the School Name using the set_index() method
12. Get the Student Count Per School, Budget Per Student, Score Averages Per School, Passing Percentages Per School
13. Create the School Summary DataFrame
14. Format and Reorder the School Summary DataFrame Columns
15. Find the Highest and Lowest Performing Schools
16. Create Grade-Level DataFrames
17. Get the Score Averages Grouped by School Name
18. Combine each grade level Series into a DataFrame, add formatting, and remove index name
19. Get per school budget, Group the Series on the Spending Ranges, and Categorize spending based on the bins using the pd.cut() method to establish the Spending Ranges per Student
20. Create a DataFrame for the Scores by School Spending
21. Create and Categorize Bins for School Size
22. Create a DataFrame for the Scores by School Size and School Type
23. Create a DataFrame for the Scores by School Type

## Results

By replacing 9th grade math and reading scores for Thomas High School with NaN, the results of our analysis changed the following:
  - District Summary: % Passing Math, % Passing Reading, and % Overall Passing changed by less than 0.2%; dropping from 75.0%, 86.0%, and 65.2% to 74.8%, 85.7%, and 64.9% respectively. While Average Math Score dropped by 0.1% from 79.0% to 78.9%, Average Reading remained unchanged at 81.9%.

District Summary including 9th Grade Thomas High School
![District_Summary_with_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118376381-435b3880-b58d-11eb-97fb-79bd3447b21c.png)

District Summary excluding 9th Grade Thomas High School
![District_Summary_without_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118376389-46eebf80-b58d-11eb-8bb7-534871077132.png)

  - School Summary: % Passing Math, % Passing Reading, and % Overall Passing changed by more than 25.0%; dropping from 93.3%, 97.3%, and 90.9% to 66.9%, 69.7% and 65.1% respectively. Average Math Score and Average Reading Score remained largely unchanged.

District Summary including 9th Grade Thomas High School
![School_Summary_with_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118376717-5838cb80-b58f-11eb-9186-75b75c3047f1.png)

District Summary excluding 9th Grade Thomas High School
![School_Summary_without_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118376719-5b33bc00-b58f-11eb-81ab-1408307a0b3f.png)

  - Top and Bottom Performing Schools: While Thomas High School's % Passing Math, % Passing Reading, and % Overall Passing dropped by 0.09%, 0.29%, and 0.32% respectively, the school still retained its second position in the top performing schools list. This is due to the fact that we recomputed the math and scores for only grade 10 to grade 12 excluding the grade 9 entirely. The list of bottom performing schools remain unchanged.

Top Performing Schools including 9th Grade Thomas High School
![Top_Performing_Schools_with_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118379364-76a6c300-b59f-11eb-9365-53f748bf130c.png)

Top Performing Schools excluding 9th Grade Thomas High School
![Top_Performing_Schools_without_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118379368-7c9ca400-b59f-11eb-8cb7-8b5f0a3aed41.png)

Bottom Performing Schools including 9th Grade Thomas High School
![Bottom_Performing_Schools_with_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118379374-86bea280-b59f-11eb-98ba-dd3ccb955749.png)

Bottom Performing Schools excluding 9th Grade Thomas High School
![Bottom_Performing_Schools_without_9th_Grade_THS](https://user-images.githubusercontent.com/67847583/118379379-8d4d1a00-b59f-11eb-9941-8e923ade8fdf.png)

