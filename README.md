# School_District_Analysis

## Project Overview

The school board has notified Maria and her supervisor that the *students_complete.csv* file shows evidence of academic dishonesty; specifically, reading and math grades for Thomas High School ninth graders appear to have been altered. Although the school board does not know the full extent of the academic dishonesty, they want to uphold state-testing standards and have turned to Maria for help. We were asked to replace the math and reading scores for Thomas High School with NaNs while keeping the rest of the data intact. Then we re-did our school district analysis to verify how these changes affected the overall analysis.

Results of First District Analysis
![district_before](Resources/district_summary_before.png)

Results of Second District Analysis
![district_before](Resources/district_summary_after.png)

There were clearly some issues with the 9th grade reading and math results at Thomas High School as can be seen in the highlighted stats from the First and Second results above.

## School District Analysis Results

The first step in the analysis was to isolate all the 9th grade reading and math scores from the students_complete.csv file (read into the student_data_df DataFrame).

We created two filters to make this step easier. The filter called 'f_ths' will isolate students at Thomas High School. The filter called 'f_9th' will isolate 9th grade students. The 'loc[]' method call is used twice on the  student_data_df DataFrame. Both times the bitwise and operator ('&') combines the 'f_9th' and 'f_ths' filters to select rows in the DataFrame. The labels "reading_score" and "math_score" are used as column selectors, in combination with the 'filter' Series as a row selector, in order to set values to 'NaN', as shown below.

![set 9th grade reading and math scores for  Thomas HS to NaN](Resources/rubric_deliverable1_50pts.png)

Validation that the previous step worked as desired, we used the 'info()' function to inspect results on the nullified results in isolation, and in comparison with the original data. Note that there were 461 nullified entries (the total number of 9th grade students at Thomas HS) out of a total of 39,170 entries (the total number of 9th-12th grade students at all District High Schools), as shown below.

![verify nullification of questionable data](Resources/rubric_deliverable1b_50pt_verify.png)

## School District Analysis Summmary

#### 1. District Summary DataFrame

Before Nullifying 9th Grade Math & Reading Scores at Thomas HS
![district_before](Resources/district_summary_before.png)

After Nullifying 9th Grade Math & Reading Scores at Thomas HS
![district_before](Resources/district_summary_after.png)

#### 2. School Summary DataFrame

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/school_summary_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/school_summary_before.png)

#### 3. Top & Bottom Five Performing Schools

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/top5_bottom5_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/top5_bottom5_before.png)

#### 4. Average Math Scores for Each Grade Level From Each School

**<font color=#ff3333>Only difference is presence of 'NaN' for Thomas HS</font>**

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/math_averages_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/math_averages_before.png)

#### 5. Average Reading Scores for Each Grade Level From Each School

**<font color=#ff3333>Only difference is presence of 'NaN' for Thomas HS</font>**

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/reading_averages_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/reading_averages_before.png)

#### 6. Scores by School Spending per students

**<font color=#ff3333>No significant difference</font>**

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/spending_summary_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/spending_summary_before.png)


#### 7. Scores by School Size

**<font color=#ff3333>No significant difference</font>**

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/size_summary_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/size_summary_before.png)

#### 8. Scores by School Type

**<font color=#ff3333>No significant difference</font>**

*After Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/type_summary_after.png)

*Before Nullifying 9th Grade Math & Reading Scores at Thomas HS*
![district_before](Resources/type_summary_before.png)
