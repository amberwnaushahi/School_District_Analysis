# School_District_Analysis

The school board informed Maria and her supervisor that the students_complete.csv file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. She has asked me to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Once I replaced the math and reading scores, Maria asked me to repeat the school district analysis that I did in this module and write up a report to describe how these changes affected the overall analysis.

*Data Source: clean_students_complete.csv, schools_complete.csv, students_complete.csv*
*Software: Python 3.7.10 
*Jupyter Notebook## 

**Overview of the School District Analysis:**

The purpose of the school district analysis is to aggregate the data and understand performance trends and patterns on all standardized test data for analysis, reporting and presentations. This will allow the school board to have informed discussions and make strategic decisions on student funding, budgets and school priorities. The initial analysis covered the performance of the students and their respective schools across several parameters. After it was discovered that the Thomas School students of the 9th grades had their scores altered, the analysis was redone by resetting scores for the 9th grade students to null.

A re-assessment of the school summaries and individual school performance showed that the modified grade 9 math and reading scores skewed the inital testing results.  The analysis was repeated using cleaned data, where all grade nine math and reading scores for Thomas High School were replaced with "NaN" values. This represented 1% of the student population test scores, amounting to 461 students out of a total of 39,170 high school students in the district. 

**Results**

**Impact on District Summary

The overall district summary saw minimal impact, affecting only the overall average math score by 0.1, overall math passing % by 0.1%, and overall reading passing % lowered by  0.1%, as seen in the tables below:

Figure 1: District_summary - Before
![image](https://github.com/amberwnaushahi/School_District_Analysis/blob/main/Analysis/district_summary_old.png)

Figure 2: District_summary - After
![image](https://github.com/amberwnaushahi/School_District_Analysis/blob/main/Analysis/district_summary_new.png)

**Impact on School Summary 

When analyzing the metrics for Thomas High School after removing the 9th grade students scores and their counts, we are able to see an Average Math Score of 83.350937, an Average Reading Score of 83.896082 and an % Overall Passing of 90.630324. Please note that the total students for 10th to 12th grades is 1175. The figures shows 1635, which is the total students for Thomas High School.

Figure 3: School_summary 
![image](https://github.com/amberwnaushahi/School_District_Analysis/blob/main/Analysis/school_summary_new.png)

**Impact on Thomas High School’s performance relative to the other schools

The grade 9 scores being replaced with NaN's did not change the school's position (which was 2nd) because the total student count remained the same as before. The instructions did not call for updating the student count in the dataframe.  

Figure 4: Top Schools
![image](https://github.com/amberwnaushahi/School_District_Analysis/blob/main/Analysis/top_5_schools_new.png)

**Affect of replacing the ninth-grade scores:

With the exception of grade 9 scores being replaced with Nan, there appears to be no change in the the scores by grade, scores by school spending, scores by school size or scores by school type. This is mostly due to the total student count remaining unchanged. I believe this analysis needs to be redone to ensure the numbers are more reflective of new student numbers. 

**Summary**

Ideally, if the correct number of students was taken into account after replacing 9th grades with NaNs, the updated school analyis would see the following changes:

* Recalculating the Average Math Score, Average Reading Score, % Passing Math, % Passing Reading and % Overall Passing considering the count and scores of students from the 10th and 12th grades only.
* Recalculating the Top 5 schools rank considering scores of students from the 10th and 12th grades only.
* Replacing the school size for Thomas High School from 1635 to 1174 in the school_data_complete_df and school_data_df DataFrames to complete the Analysis by school spending, school size and school type.
* Creating a new tier on the bins to include schools with spending ranges per students above 676, as Thomas High School's spending range per student would likely increase due to fewer number of students
