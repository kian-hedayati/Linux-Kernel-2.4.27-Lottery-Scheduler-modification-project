# Linux-Kernel-2.4.27-Lottery-Scheduler-modification-project
# Lottery Scheduler Implementation – Linux Kernel 2.4.27

## Course
CSE331 Operating Systems Design – Fall 2025

## Authors
- Kian Hedayati
- Shahin Adami

## Project Overview
This project modifies the Linux 2.4.27 scheduler to implement a dynamic Lottery Scheduler with user-fair CPU distribution.

## Features
- Added new scheduling policy
- Implemented ticket-based dynamic fairness
- Added new system call to switch scheduler
- Performance instrumentation
- CPU utilization & MSE comparison

## Kernel Modifications
Modified files:
- kernel/sched.c
- include/linux/sched.h
- kernel/fork.c
- modifiedscheduler.c (new system call)

## Compilation
1. Patch kernel
2. Rebuild kernel
3. Install
4. Reboot

## Testing
- Used CPU-intensive infinite loop
- Collected CPU data using:
- - Analyzed using AWK

## Results
Lottery scheduler shows probabilistic fairness with higher MSE compared to default scheduler.

## Conclusion
User-based lottery scheduling is viable but introduces probabilistic variance.
