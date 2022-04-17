# School District Analysis

## Project Overview
---

### Purpose
Analyzing school district for the school board utilizing Pandas. It has been decided to change the 9th grade math and reading scores from Thomas High School to NaN with evidence found that the 9th grade scores from Thomas High School have been altered. After altering the Thomas High School data, the school district analysis was redone to completion.

### Resources
[loc method - Pandas](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.loc.html)

[Pandas formatting DataFrame](https://www.geeksforgeeks.org/formatting-integer-column-of-dataframe-in-pandas/#:~:text=Let%E2%80%99s%20see%20different%20methods%20of%20formatting%20integer%20column,commas%20and%20Dollar%20sign%20with%20two%20decimal%20places.)

## Results
---

### School Results

#### District Summary
The district summary registered small changes to score averages and passing percentages. 

- School count, Total student count, and Total budget remained unchanged.
- Average Math and Average Reading Scores changed, but a small amount.
  - Average Math: 79.0 to 78.9
  - Average Reading: 81.9 to 81.9 (neglegable change)
- % Passing Math And Reading changed, but a small amount.
  - % Passing Math: 75.0 to 74.8
  - % Passing Reading: 85.8 to 85.7
  - % Overall Passing: 65.2 to 64.9



#### School Summary
The school summary wasn't greatly impacted outside of Thomas High School. With the reading and math scores being adjusted, the averages and percentages of all schools were slightly lowered, except for the Average Reading Score which rose by .03. The score averages across all schools weren't impacted greatly. 

##### All Schools
- Average Math Score: 80.4 to 80.4
- Average Reading Score: 82.5 to 82.5
- % Passing Math: 81.0 to 79.2
- % Passing Reading: 89.2 to 87.4
- Overall Passing Percentage: 73.3 to 71.6

Before replacing 9th grade scores

![Initial_School_Summary](Resources/THS_old_school_summary.png "Old School Summary")

After replacing 9th grade scores

![New_School_Summary](Resources/THS_new_school_summary.png "New School Summary")

#### Thomas High School Impact
The reading and math score values for Thomas High School 9th graders were changed to NaN values. This reduced the amount of Thomas High School students by 461 students. The change in student count (from 39,170 to 38,709) impacted the Average Reading and Math Scores, % Passing Reading and Math, and % Overall Passing. **The significant change was to passing percentages** As shown below, taking out the 9th grade scores dropped the schools passing percentages by 28.4%. 

- Average Math Score: 83.4 to 83.4
- Average Reading Score: 83.8 to 83.9
- **% Passing Math: 93.3 to 66.9**
- **% Passing Reading: 97.3 to 69.7**
- **% Overall Passing: 90.9 to 65.1**

To fix this considerable change in passing percentages, the Thomas High School 9th graders were taken out of the calculations for passing grades. The 10th, 11th, and 12th graders were the only students considered in grade percentage calculations. 

##### Thomas High School - Performance

- % Passing Math: 66.9 to 93.2
- % Passing Reading: 69.7 to 97.0
- Overall Passing %: 65.1 to 90.3 

As issustrated, the refactored grade percentages closely match the original % calculations before changing the 9th grade scores to NaN values.

###### Thomas High School - Impact on ranking

- Thomas High School has a 2nd place ranking (90.63%) overall passing
  - This is the same ranking as before replacing Thomas High School's 9th grade scores
- If the total Thomas High School student count was calculated (including 9th graders) the rank would have dropped to 8th overall.

#### Impact on replacing ninth grade scores


##### Math by Grade



![Math_by_grade](Resources/math_grade_performance.png "Math Performance by Grade")

##### Reading by Grade

![Reading_by_grade](Resources/reading_grade_performance.png "Reading Performance by Grade")


##### School Spending


- The higher the school spending, the lower the performance.
- When digging deeper, the overall budget for district type schools is considerable higher as is the student count. 

![Spending_summary](Resources/spending_summary.png "Spending Summary")

##### School Size

As shown in the range below, small and medium sized schools have relative success compared to larger schools. Medium sized schools (1000-1999 students) were the only category to change, and it was less than .5%. The large and small size schools were impacted. This is due to Thomas High School being a middle sized school.

- Both small and medium school ranges (0-999, 1000-1999) average an Overall Passing % of 90.5%. 
- Large schools (2000-5000) have an Overall Passing % of 58%

![Size](Resources/school_size_performance.png "School Size Summary")

##### School Type

School type demonstrates that charter schools earn higher grade score averages. Even more significant is the % Overall Passing difference; Charter passing 90% of their students while District schools pass 54%. There is a correlation to school size as every district school is large in size (2000-5000 students). While technically the performance changed per school type, it's a neglegable amount. 


![Type](Resources/school_type_performance.png "School Type Summary")

## Summary
---
Theere have been changes to Thomas High School math averages, reading averages, math passing percentage, reading passing percentage, and overall passing percentage. The differences are minute, but present. The student count for Thomas High School has been adjusted to exclude 9th graders to more accurately calculate results. The overall passing percentage initially had the most significant change before changing calculations to exclude the 9th grade scores from calculations. There are NaN values shown in both the Thomas High School math and reading score by grade images.


