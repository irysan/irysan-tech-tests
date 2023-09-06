## Context

A system regularly registers tests, students, their test submissions and the grades each test has received.

Students can submit more than one test per day, and can submit the same test more than once.

Tests can optionally be graded, with grades ranging from 0-100. If a test is graded with a 0, it was deemed invalid.

## Problem

We need to know:

* The number of unique students who submitted at least 1 test each day, for the last 15 days.
* The number of unique students who submitted at least 1 valid test each day, for the last 15 days.
* The student with the most submissions for each day of the last 15 days. If there are two or more students with the same results, print the student with the lowest ID.
* The average grade for each test. If a student has submitted just once, consider that grade regardless of its value. If the student submitted the same test multiple times, give preference to the last valid grade.

## Solution

The solution can be developed in any programming language you'd like (Python, SQL, Ruby, etc.).
It will have to ingest the data and print on the console the answers for the problems above.

You should provide the script (or scripts) you developed, and a Dockerfile for us to run your script.
