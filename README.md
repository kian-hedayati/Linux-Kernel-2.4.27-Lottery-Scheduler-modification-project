# Lottery Scheduler -- Linux Kernel 2.4.27 (CSE331 Phase II)

Implementation of a dynamic Lottery Scheduler for Linux Kernel 2.4.27 as
part of CSE331 Operating Systems Design (Fall 2025).

## Authors

-   Kian Hedayati (20220702148)
-   Shahin Adami (20210702127)

## Project Overview

This project modifies the default Linux scheduler to support
ticket-based probabilistic Lottery Scheduling. A custom system call is
implemented to switch between the default scheduler and the lottery
scheduler for testing and evaluation.

## Key Features

-   Ticket-based process selection
-   Dynamic ticket adjustment based on CPU usage
-   Custom system call for scheduler switching
-   Performance comparison using CPU utilization and MSE analysis

## Modified Kernel Components

-   kernel/sched.c
-   include/linux/sched.h
-   kernel/fork.c
-   modifiedscheduler.c (new system call)

## Repository Structure

kernel_modifications/ Modified kernel source files only\
user_programs/ Test programs (loop.c, test.c)\
scripts/ Data analysis scripts\
results/ Output logs and graphs\
report/ Final project report

## Build & Run (High-Level)

1.  Start with a clean Linux 2.4.27 source tree.
2.  Apply modifications (or patch file).
3.  Build and install the kernel.
4.  Reboot into modified kernel.
5.  Use the provided user-space program to switch scheduler mode.
6.  Run CPU-bound processes and collect performance data.

## Testing Example

Collect CPU usage samples:

    top -n 100 -d 1 -b > output.txt

## Summary

The Lottery Scheduler introduces probabilistic fairness, leading to
higher short-term variance compared to the deterministic default
scheduler, while maintaining fairness over time.
