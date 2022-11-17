# A Comparative Analysis of Standardized Test Results Between CA School Boards
--- 
### College-Readiness Benchmarks as a Barometer of Access and College Preparation
---
## Problem Statement

*The Mayor would like to "move the needle on education". Our firm has been brought in to make recommendations on the best course of action. We will endeavor to use SAT/ACT enrollment and benchmark performance between California school districts in 2018-2019 order to analyze district-level causal factors for over and under performance, with the goal of recommending the most effective and equitable course of action to the town education board.*

## Summary

A broad-spectrum analysis of SAT/ACT performance by California School district is undertaken, using the percent of students scoring at or above the SAT and ACT college-readiness benchmark scores as the primary metric. This report attempts to explain college-readiness benchmark under and overperformance at the school district level through the analysis of enrollment metrics, teacher demographic metrics-such as overall level of teacher education, student-to-teacher ratio and years teaching, as well as school district fiscal data.

## Data Dictionary

| DataFrame            | Description                                                              |
| -------------------- | ------------------------------------------------------------------------ |
| sat_2019_ca          | SAT scores and metrics by school district for 2018-19.                   |
| act_2019_ca          | ACT scores and metrics by school district for 2018-19.                   |
| staff_demo_1819      | A large dataframe of every registered teacher in CA.                     |
| current_expense_1819 | Fiscal info for every school district in CA for the 2018-19 school year. |
| cenroll_1819         | Student enrollment and demographic data by school district for 2018-19.  |
| ca_edu_stats_1819    | Cleaned dataframe merged as appropriate from the above.                  |

---

| Feature                         | Type  | Dataset                   | Description                                                                                                                                                                                                                                                                                                                          |
| ------------------------------- | ----- | ------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| d_name                          | str   | All                       | The school district within California.                                                                                                                                                                                                                                                                                               |
| sat_enroll                      | float | CA 2019 SAT               | The number of 12th graders enrolled to take the SAT in 2018-2019.                                                                                                                                                                                                                                                                    |
| sat_num_tst_taker               | float | CA 2019 SAT               | The count of 12th graders that took the SAT in 2018-2019.                                                                                                                                                                                                                                                                            |
| sat_num_erw_over_benchmark      | float | CA 2019 SAT               | The count of 12th graders that exceeded the readiness benchmark in exploratory reading and writing(erw).                                                                                                                                                                                                                        |
| sat_pct_erw_over_benchmark      | float | CA 2019 SAT               | The percent of 12th graders that exceeded the readiness benchmark in exploratory reading and writing(erw).                                                                                                                                                                                                                      |
| sat_num_math_over_benchmark     | float | CA 2019 SAT               | The count of 12th graders that exceeded the readiness benchmark in math.                                                                                                                                                                                                                                                        |
| sat_pct_math_over_benchmark     | float | CA 2019 SAT               | The percent of 12th graders that exceeded the readiness benchmark in math.                                                                                                                                                                                                                                                      |
| sat_tot_num_both_over_benchmark | float | CA 2019 SAT               | The count of 12th graders that exceeded the readiness benchmark in math and erw.                                                                                                                                                                                                                                                |
| sat_pct_both_over_benchmark     | float | CA 2019 SAT               | The percent of 12th graders that exceeded the readiness benchmark in math and erw.                                                                                                                                                                                                                                              |
| annual_expense_of_ed            | float | CA School District Fiscal | Total general fund expenditures less food services, facilities acquisition and construction and certain other terms, divided by (ADA). <br/> The total days of student attendance divided by the number of instructional days in the year.                                                                                           |
| current_expense_per_ada         | float | CA School District Fiscal | annual_expense_of_ed divided by ADA -- the per-pupil cost of education per school board for 2018-2019.                                                                                                                                                                                                                               |
| lea_type                        | str   | CA School District Fiscal | Type of school district.                                                                                                                                                                                                                                                                                                             |
| avg_tchr_sex                    | float | CA Teacher Demographics   | Average sex of teachers within school district.                                                                                                                                                                                                                                                                                      |
| avg_tchr_edu_lvl                | float | CA Teacher Demographics   | Average level of education held by teachers within school district. <br/> 10 = Doctorate, 9 = Special, 8 = Master's + 30 or more semester hours, 7 = Master's, 6 = 5th year within bachelor's,<br /> 5 = 5th year induction, 4 = 5th year, 3 = Bachelors + 30 or more semester hours, 2 = Bachelors, 1 = Associate, 0 = Not reported |
| avg_tchr_yrs_tching             | float | CA Teacher Demographics   | Average number of years as a teacher.                                                                                                                                                                                                                                                                                                |
| avg_tchr_yrs_in_dstrct          | float | CA Teacher Demographics   | Average number of years teaching within that specific school district.                                                                                                                                                                                                                                                               |
| tchrs_per_district              | int   | CA Teacher Demographics   | Total number of teachers per school district.                                                                                                                                                                                                                                                                                        |
| cumulative_enrollment           | float | CA Student Enrollment     | Total number of students enrolled per school district.                                                                                                                                                                                                                                                                               |
| student_teacher_ratio           | float | CA Student/CA Teacher     | Average student to teacher ratio per school district.                                                                                                                                                                                                                                                                                |
| cum_enrollment_sed              | float | CA Student                | Total number of socioeconomically disadvantaged students/district.                                                                                                                                                                                                                                                                   |
| socio_ec_disadv_pct             | float | CA Student                | The percent of students that are socioeconomically disadvantaged/district.                                                                                                                                                                                                                                                           |
| act_enroll                      | float | CA 2019 ACT               | The number of 12th graders enrolled to take the ACT in 2018-19.                                                                                                                                                                                                                                                                      |
| act_num_tst_takr                | float | CA 2019 ACT               | The number of 12th graders that took the ACT in 2018-19.                                                                                                                                                                                                                                                                             |
| act_avg_scr_read                | float | CA 2019 ACT               | Average ACT reading score.                                                                                                                                                                                                                                                                                                           |
| act_avg_scr_eng                 | float | CA 2019 ACT               | Average ACT english score.                                                                                                                                                                                                                                                                                                           |
| act_avg_scr_math                | float | CA 2019 ACT               | Average ACT math score.                                                                                                                                                                                                                                                                                                              |
| act_avg_scr_sci                 | float | CA 2019 ACT               | Average ACT science score.                                                                                                                                                                                                                                                                                                           |
| act_num_ge_21                   | float | CA 2019 ACT               | The count of 12th graders scoring in excess of the ACT benchmark.                                                                                                                                                                                                                                                                    |
| act_pct_ge_21                   | float | CA 2019 ACT               | The percent of 12th graders that exceeded the ACT readiness benchmark.                                                                                                                                                                                                                                                                                                                                     |
