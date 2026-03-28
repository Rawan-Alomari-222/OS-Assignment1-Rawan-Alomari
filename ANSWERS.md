# Assignment Questions

## Instructions
Answer all 4 questions with detailed explanations. Each answer should be **3-5 sentences minimum** and demonstrate your understanding of the concepts.

---

## Question 1: Thread vs Process

**Question**: Explain the difference between a **thread** and a **process**. Why did we use threads in this assignment instead of creating separate processes?

**Your Answer:An autonomous program with its own memory and system resources is called a process. Within a process, a thread is a smaller unit of activity that shares memory with other threads. Threads are quicker and lighter than processes, which are heavy and need more time to make. Unlike processes, threads share memory, which facilitates communication. We chose threads in this assignment because they make it easier to transition between jobs and are more effective at imitating CPU scheduling.
**

[Write your answer here. Consider: What is a process? What is a thread? How do they differ in terms of memory, resources, creation overhead? Why are threads more suitable for this simulation?]

---

## Question 2: Ready Queue Behavior

**Question**: In Round-Robin scheduling, what happens when a process doesn't finish within its time quantum? Explain using an example from your program output.

**Your Answer:In Round-Robin scheduling, if a process does not finish within its time quantum, it is moved to the end of the ready queue. This allows other processes to execute before it gets another turn. The process will wait in the queue until it is scheduled again by the CPU. This ensures fairness among all processes. The process continues repeating this cycle until it finishes execution.**



Example from my output:
```
P2 executing quantum [4000ms]
P2 completed quantum 4000ms │ Overall progress: [█████████░░░░░░░░░░░] 46%
Remaining time: 4519ms
P2 yields CPU for context switch

P2 (Priority: 1) added to ready queue




```

**Explanation of example:**
In this instance, process P2 failed to finish in the allotted 4000 milliseconds. It still requires additional CPU time to complete, as evidenced by the remaining time (4519 ms). As a result, it returns to the ready queue after yielding the CPU. This implies that while other processes run, it will wait for its next turn. This behaviour illustrates how Round-Robin scheduling guarantees efficient CPU sharing and fairness.

---

## Question 3: Thread States

**Question**: A thread can be in different states: **New**, **Runnable**, **Running**, **Waiting**, **Terminated**. Walk through these states for one process (P1) from your simulation.

**Your Answer:**
During execution, process P1 in this simulation goes through several thread states. When P1 is first produced and added to the ready queue ("P1 (Priority: 3) added to ready queue"), it is in the New state. When the scheduler chooses it and it is prepared to execute, it becomes Runnable. The Running state is reached when execution begins ("P1 executing quantum [4000ms]"). If it doesn't finish, it waits for its next turn in the ready queue and yields the CPU ("P1 yields CPU for context switch"). When P1 finishes running ("P1 finished execution!"), it finally reaches the Terminated state.


1-New: When P1 is created and added to the ready queue.
2-Runnable: When P1 is ready and waiting to be scheduled by the CPU.
3-Running: When P1 starts executing ("P1 executing quantum [4000ms]").
4-Waiting: When P1 yields the CPU and waits in the ready queue.
5-Terminated: When P1 finishes execution ("P1 finished execution!").
---

## Question 4: Real-World Applications

**Question**: Give **TWO** real-world examples where Round-Robin scheduling with threads would be useful. Explain why this scheduling algorithm works well for those scenarios.

**Your Answer:**

### Example 1: Web Browsers

**Description**: 
Web browsers handle multiple tasks such as loading pages, playing videos, and user interaction at the same time.

**Why Round-Robin works well here**: 
Round-Robin ensures that each task gets a fair share of CPU time. This improves responsiveness and prevents freezing. It allows smooth multitasking between tabs. The fairness makes it suitable for interactive applications.

### Example 2: Operating Systems Scheduling

**Description**: 
Operating systems manage multiple processes running simultaneously.


**Why Round-Robin works well here**: 
Round-Robin gives each process equal CPU time. This prevents starvation and improves system performance. It is useful in time-sharing systems. The predictable behavior makes scheduling efficient.


---

## Summary

**Key concepts I understood through these questions:**
1-Difference between threads and processes
2-Round-Robin scheduling and queue behavior
3-Thread lifecycle and execution

**Concepts I need to study more:**
1-Thread synchronization
2-Advanced scheduling techniques
1. 
2. 
