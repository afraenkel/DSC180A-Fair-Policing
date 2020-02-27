Assignment #3: Cleaning and EDA (Due March 14, 11:59 PM)
===============================

In this assignment you will:

1.  Describe the experimental design and write a summary of the results with code-generated figures and tables (report)

2.  Develop code to replicate the main result under consideration, using methodological best practices from class (code)

* * * * *

This project consists of the entire 'result replication' as a single
report and code artifact. You should put together the work from
assignments 1 and 2, along with additional material from more recent
work. You previous work should be considered a *rough draft* of the
final work you are turning in for assignment 3.

### Part 1 (Report)

Create a report consisting of:
* An introduction to the problem (assgn 1)
* An introduction to the data and data generation process (assgn 1)
* A brief review of historical context (assgn 1)
* EDA, assessment of reliability of data, need for cleaning and
  justification for approach to cleaning. (assgn 2)
* Careful analysis in differences in stop rates (assgn 2)
* Careful analysis of post-stop outcomes (assgn 2)
* Explanation and calculation of Veil of Darkness experiment (assgn 2).
* Critique of the short comings of the VoD, and likely quantitative
  effect of those shortcomings on the results (**new**).
* Moving beyond the SDSU study by looking at main results
  year-after-year (**new**).
* Conclusion (**new**).

### Part 2 (Code)

Develop code in a GitHub repository that replicates the main result of
question at hand. This repository will run the replication from
end-to-end (data ingestion to generating the results that inform the
reports) using best-practices described in class.

You code should satisfy the following criteria:
* Conform to the template structure of the methodology portion of the
  course.
* Use configuration files to parameterize the inputs of your pipeline.
* Use a `run.py` file to put together the processing logic, using
  commandline targets.
* Runnable on the DSMLP servers in an existing Docker Image (either on
  given to you (e.g. `ucsd-ets/scipy-ml`, or one created by you).
* Use a small amount of versioned test data that quickly verifying the
  runnability of the project.
* A configuration file `config/env.json` that contains the following
  information:
  * a key `docker-image` with the value a DockerHub path (e.g. the
    input of the `-i` flag when starting a container on the DSMLP
    server.
  * a key `output-paths` with the value a list of output files created
    (the files with the results of the replication).
* All criteria specified in assignments 1 and 2.

Your code will be turned into gradescope directly from
GitHub. Alongside inspecting the files of the repository, it will
be graded using the following procedure:

1. Your submitted repository will be uploaded to a DSMLP server.
2. A container will be started using the specified Docker Image in
   your repository's `env.json`
3. In this container, the following command will be run: `python
   run.py test-project`
4. Running the above target will run your replication on a small
   amount of test data. The existence/content of output test files
   will be checked.

*Note:* You should test running your project from end-to-end, by
pulling it from GitHub and trying to run the targets yourself, in a
clean directory! (E.g. create a directory `~/test-run/`, and clone/run
the project in that directory).
