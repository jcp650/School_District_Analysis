# School District Analysis

## Project Overview

This project was tasked by the Chief Data Scientest for a school district for the purpose of analyzing standardized testing data in relation to school size, type and funding. The results of this analysis are designed to reveal trends and patterns that can inform the School Board and District Superintendents about budget decisions at the district and school levels. Specifically, the relationship between standardized test performance and school budget, size and type will advise future budgeting decisions to ensure all students have the same level of support necessary to succeed.

## Results

After the initial analysis was performed, the School Board informed the Chief Data Scientist that academic dishonesty occurred at Thomas High School among students in ninth grade. The best course of action to preserve the data quality was to change the Thomas High School's ninth grade scores to NaN values, which excluded them from calculations. The code used to convert Thomas High School Math and Reading scores to NaN values was:
```
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "reading_score"]=np.nan
student_data_df.loc[(student_data_df["school_name"] == "Thomas High School") & (student_data_df["grade"] == "9th"), "math_score"]=np.nan
```
Below will be a discussion of changes made to the analysis as well as how these changes affected the final analysis results. 

### District Summary

The district summary was slightly affected by the removal of Thomas High School's ninth grade test scores. All of the metrics decreased except for the average reading score. **Figure** 1 shows the district summary before removing the Thomas High School ninth grade scores, and **Figure 2** shows the district summary after removing the scores.


