# School_District_Analysis
School District analysis for Bootcamp

## Overview
The school board notified us that the math grades for the 9th grade of the Thomas High School has been compromised. This causes a problem because it affects all the data we gathered before. Our approach to correcting the dishonest act, will be to replace the Thomas High School 9th grade with NaN values, which is missing value. The rest of the DataFrame will be kept intact. We created this report in order to find the differences between the "dishonest" data and the new data.

## Results:
#### How is the district summary affected?
- As we can see in the chart below, we can spot a very few differences. Since we kept all the students names, the student count and budget remains practically the same. We can see a small drop in the math average score. The reading average score remains pretty much the same. We can see a drop in the 3 percentages. Using 1 decimal we can observe that the math percentage fell by .2 points, meanwhile the reading fell by .1 and the overall by .3 points. 

*Dishonest Data* 
<img width="923" alt="Captura de Pantalla 2021-07-18 a la(s) 16 51 46" src="https://user-images.githubusercontent.com/85461477/126083184-03b47cb5-1a59-4ff8-be9d-a0607bf6de8e.png">

*New Data*
<img width="919" alt="Captura de Pantalla 2021-07-18 a la(s) 16 46 59" src="https://user-images.githubusercontent.com/85461477/126083110-ce6a5672-92db-46ad-9741-03623e54ce2e.png">

#### How is the school summary affected?
- Naturally, most of the data was left untouched, only the Thomas High School Data was modified, therefore un the per_school_summary, only the THS Data is different in both DataFrames. In the charts below, we can see the difference between the data. As we know the School Type, Total Schools and both Budgets columns stayed the same. We can see a small drop in the average grades and a slight increase in the reading average grade, for the THS. We can see big drops in the percentages, ranging from aprox. 25% to 29%.

*Dishonest Data* 
<img width="975" alt="Captura de Pantalla 2021-07-18 a la(s) 17 14 14" src="https://user-images.githubusercontent.com/85461477/126083769-f542d7ec-0578-4bf8-b034-694ea4005922.png">
*New Data*
<img width="968" alt="Captura de Pantalla 2021-07-18 a la(s) 17 14 26" src="https://user-images.githubusercontent.com/85461477/126083771-f223d4fa-1c5a-4547-92e4-f55eed2a15bb.png">


#### How does replacing the ninth graders’ math and reading scores affect Thomas High School’s performance relative to the other schools?
- As we can See in the previous DataFrames, We can see the average of students passing dropping drastically, from 93.272171% to 66.911315% of students passing math, a drop from 97.308869% to 69.663609% of students passing reading, and an overall passing percentage dropping from 90.948012%.

#### How does replacing the ninth-grade scores affect the following:
- Math and reading scores by grade: As we can see in the Chart bellow, the only difference between both DataFrames si that the average score by grade, is that 9th grade in Thomas High School is NaN, rather than a number. (the charts are the math_scores_by_grade DataFrames, the former is the dishonest and the latter is de new chart.) <img width="310" alt="Captura de Pantalla 2021-07-18 a la(s) 20 29 40" src="https://user-images.githubusercontent.com/85461477/126090239-5c0db148-c929-4240-a389-912113023db5.png"><img width="302" alt="Captura de Pantalla 2021-07-18 a la(s) 20 29 29" src="https://user-images.githubusercontent.com/85461477/126090247-76d6c0e6-e1bb-4f1a-8b69-33c12ee7f8b4.png">

- Scores by school spending: In the Charts bellow we can see the different Dataframes. If we take a look at the at the formatted dataframes, we can see there is no significant difference. It may look like there's no difference, however if analyze de data for the "$630 - $644" to the 1/1000000 we can see there is a difference of .079423 for the overall passing percentage. There are also marginal changers in average math score, average reading score, % passing math and % passing reading., <img width="811" alt="Captura de Pantalla 2021-07-18 a la(s) 20 44 50" src="https://user-images.githubusercontent.com/85461477/126092000-616bf7f8-4a27-4a08-bc28-968a22815d5c.png"> <img width="812" alt="Captura de Pantalla 2021-07-18 a la(s) 20 45 07" src="https://user-images.githubusercontent.com/85461477/126092002-187b55a3-5728-4edf-a84b-e1cc4bc7dc2d.png">

- Scores by school size: Since Thomas High School is a medium sized school, we can see something similar to what we saw in the "Scores by school spending". if we analyze the data without fractions, the results are practically the same. When we analyze the data to the 1,000,000th, we can see the scores lowering a little bit. <img width="751" alt="Captura de Pantalla 2021-07-18 a la(s) 21 04 41" src="https://user-images.githubusercontent.com/85461477/126092742-9ad68ce0-3494-41d3-938c-e0f872fe787d.png"> <img width="747" alt="Captura de Pantalla 2021-07-18 a la(s) 21 04 52" src="https://user-images.githubusercontent.com/85461477/126092744-e523e472-9147-42dc-9a56-319d0d142539.png">

- Scores by school type: Beacuse Thomas High School is a "Charter School", we can see the same as in the same results as in the "Scores by school size" and "Scores by school spending". When we analyze the formatted Dataframe, we see that the data looks identical, yet if we analyze the data without the format, we can see a little dunk in the Charter school rows. Here we can see the two dataframes without format, the first is the dishonest data, the second is the new data. <img width="702" alt="Captura de Pantalla 2021-07-18 a la(s) 21 11 49" src="https://user-images.githubusercontent.com/85461477/126093069-9b12fb16-73e2-45ff-bcee-770b2ff8d294.png"> <img width="701" alt="Captura de Pantalla 2021-07-18 a la(s) 21 11 37" src="https://user-images.githubusercontent.com/85461477/126093067-63de27cc-dfbd-45f7-967a-6862ccf2552e.png">


## Summary 
The four main changes we can see when excluding the 9th grade math and reading scores for Thomas High School are the following:
- The main change is a drop in the passing percentage of the school. We can see the percentage dropping from approximately 25% to 29%.
- We can see that the reading scores for 9th grade in the THS are nonexistent. (Which is the main point of the exercise)
- We can observe that, beacuase the categories have thousands od students, the scores of the "school type", "school size", and "school spending", change just a little percentage, almost invisible if we work with no decimals.
- We can see a small change in the district performance.
The main takeaway of the analysis is that a dishonest piece of information can change the output of a well done analysis, and while working with large numbers, changes can appear like nonexistent, they exist and hurt our analysis.
