# Development Log

## Instructions
Document your development process as you work on the assignment. Add entries showing:
- What you worked on
- Problems you encountered
- How you solved them
- Time spent

**Requirements**: Minimum 5 entries showing progression over time.

---

## Example Entry Format:

### Entry 1 - [March 27, 2026, 3:00 PM]
**What I did**: Started working on the assignment and ran the initial code

**Details**: 
-Opened the project in VS Code
-Updated my student ID in the code
-Ran the program to understand how the scheduler works
-Observed how processes are added to the ready queue

**Challenges**:
Git was not recognized in the terminal

**Solution**:
Installed Git and verified it using git --version

**Time spent**:45 minutes

---

## Your Development Log:

### Entry 1 - [Date and Time]
**What I did**: 

**Details**: 

**Challenges**: 

**Solution**: 

**Time spent**: 

---

### Entry 2 - [March 27, 2026, 8:00PM]
**What I did**: Understood the Round-Robin scheduling logic

**Details**: 
-Analyzed how the ready queue works
-Followed execution of processes in the output
-Observed how processes are re-added when not finished

**Challenges**: Understanding how processes move in and out of the queue

**Solution**: Carefully traced the output step by step

**Time spent**: 2 hours

---

### Entry 3 - [March 28, 2026, 1:30 AM]
**What I did**: Implemented Feature 1 (Priority)

**Details**: 
-Added priority attribute to Process class
-Generated random priority values
-Displayed priority in the output

**Challenges**: Ensuring priority is passed correctly in constructor

**Solution**: Modified constructor and tested multiple runs

**Time spent**: 1.5hours

---

### Entry 4 - [March 28, 2026, 2:30 AM]
**What I did**: Implemented Feature 2 (Context Switch Counter)

**Details**: 
-Added counter variable for context switches
-Incremented counter before each process execution
-Displayed total at the end

**Challenges**: Finding the correct place to increment the counter

**Solution**: Placed it before currentThread.start()

**Time spent**: 1 hours

---

### Entry 5 - [March 28, 2026, 3:30 AM]
**What I did**: Implemented Feature 3 (Waiting Time)

**Details**: 
-Added variables to track waiting time
-Used methods to record enqueue and start time
-Printed waiting time summary at the end

**Challenges**: Incorrect waiting time calculation at first

**Solution**: Used timestamps (System.currentTimeMillis()) correctly

**Time spent**: 1.5 hours

---

### Entry 6 - [March 28, 2026, 7:00 AM]
**What I did**: Debugging and final testing

**Details**: 
-Fixed duplicate process names in output
-Used HashSet to remove duplicate waiting time entries
-Tested program multiple times
-Verified final output correctness

**Challenges**: Duplicate entries in waiting time summary

**Solution**: Used HashSet to ensure unique processes

**Time spent**: 1 hours

---

## Summary

**Total time spent on assignment**: [2 days]

**Most challenging part**: 
The most challenging part was implementing the waiting time feature correctly and understanding how to track process execution over time.

**Most interesting learning**: 

The most interesting part was understanding how Round-Robin scheduling works in practice and how processes share CPU time.

**What I would do differently next time**: 

I would test each feature step by step earlier and spend more time understanding the logic before coding.
