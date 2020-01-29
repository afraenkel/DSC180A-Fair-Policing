Assignment #2: Cleaning and EDA (Due Feb 14, 11:59 PM)
===============================

In this assignment you will:

1.  Statistically assess the quality of the data, justify the
    data-cleaning logic, and explain/analyze the
    features/statistics/target needed for the replication (report).
    
2.  Develop and justify data cleaning (code).

* * * * *

### Part 1

* (Cleaning) Perform an initial EDA to statistically assess the quality of the data
and its appropriateness for addressing the problem at hand, **justifying
data cleaning logic**. This will likely address issues with accuracy,
precision, and missingness of specific attributes, tying these issues
to their possible impact over eventual results.

* (Descriptive Stats) Statistically summarize the relevant, cleaned attributes and derived
features (e.g. in univariate and bivariate analyses) for San Diego.

* (Traffic Stop Analysis) Calculate and document the differences in
  stop rates and post-stop outcomes. The analysis should address
  possible reasons for such differences (including addressing possible
  confounders). Additionally:
      - The significance of these differences should be tested using
        statistical inference.
      - These differences should also be calculated across other
        variables of interest (e.g. service area).
        
* (Veil of Darkness) Perform the Veil of Darkness analysis for San
  Diego. Include an introduction to the technique and interpret the
  results. (In Assignment #3 you will carefully address the
  shortcoming of this result.)


### Part 2

Develop code to clean data (as defined and justified in Part 1),
create the features for the replication, and compute the statistics
for the report. Such code should conform to the methodology portion
of the course (e.g. using the project template).

In particular, your project should have a `run.py` with the following
targets:
1. `data` creates the data needed for analysis.
2. `process` cleans and prepares the data for analysis (e.g. cleaning
   and feature creation).
3. `data-test` ingests a small amount of *test data* (that `process`
   can then process).
