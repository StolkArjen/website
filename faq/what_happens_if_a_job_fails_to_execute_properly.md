---
title: What happens if a job fails to execute properly?
layout: default
tags: [faq, peer]
---

## What happens if a job fails to execute properly?

Your peer master records the time at which jobs are submitted. When the finished job returns, the time is also recorded. This allows the peer master to create a list of all execution times. 

Once all jobs have been submitted, but not all jobs have returned, the peer master will start checking the execution time of non-finished jobs that still have to return. It compares the time that the job was submitted with the expected return time. The expected return time is estimated from the distribution of all finished jobs (see below). If the non-finished job takes significantly longer to return, then it will be resubmitted to another peer slave.

By default the expected time for a job to return is set at the maximum execution time of all finished jobs, plus the range (the maximum minus the minimum) of the execution times. This resembles the mean plus two times the standard deviation. 

If the evaluation of your function on the slave results in an error, that error is caught and sent back to the peer master where it will be displayed. In this case the job is not resubmitted, because (most likely) the same error would happen. 
