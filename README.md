# algo-crew-scheduling-mini-project-sunisha_udar
✈️**Airline Crew Scheduling using Backtracking**

**NP-Hard Problem Modeling • Constraint Satisfaction • Profiling & Visualization**

📌 **Overview**

Airline crew scheduling is a real-world NP-hard resource allocation problem. It involves assigning flights to crew members while satisfying constraints such as non-overlapping schedules and mandatory rest times.
This mini-project implements a simplified version of this scheduling problem using a backtracking algorithm, allowing performance analysis and visualization.

🎯 **Learning Objectives**

By completing this project, you will:

Understand how scheduling problems map to NP-hard constraint satisfaction problems

Apply backtracking to explore valid crew–flight assignments

Analyze computational growth as problem size increases

Measure time complexity and recursive depth

Visualize schedules using Gantt charts and profiling graphs

Document algorithmic strategy and trade-offs

🧩 **Problem Description**

You are given:

✈️ **Flights**

A list of flights in the format:

('FlightID', start_time, end_time)


**Example:**

flights = [('F1', 9, 11), ('F2', 10, 12), ('F3', 13, 15)]

 **Crew Members**

Example:

crew_members = ['C1', 'C2', 'C3']

✔️ **Constraints**

Your scheduling must satisfy:

No overlapping flights assigned to the same crew

Minimum rest time of 1 hour between flights

(Optional) Cost minimization or fairness optimization

🛠️ **Approach / Methodology**

1️⃣ **Constraint Checking**

A function verifies whether a crew member can take a new flight:

No time overlap

At least 1 hour difference between flights

2️⃣ **Backtracking Algorithm**

Recursively try assigning each flight to any crew member

If constraints violate → backtrack

Explore all valid combinations until a valid full assignment is found

3️⃣ **Random Flight Generation**

To test varying input sizes, flights are generated randomly within a time window.
The random times ensure every run is different and produce natural complexity growth.

4️⃣ **Profiling**

For input sizes 4 to 10 flights, measure:

Execution time

Number of recursive calls

Plot exponential growth due to NP-hard nature.

5️⃣ **Visualization**

A Gantt Chart shows crew timelines:

Each crew is a horizontal bar

Flights appear as color-coded segments

📊 **Output Example**
{
    'C1': ['F1', 'F4'],
    'C2': ['F2', 'F5'],
    'C3': ['F3']
}

📉 **Performance Graphs**

**The project generates:**

🔹 **Execution Time vs. Number of Flights**

Demonstrates exponential time increase due to backtracking.

🔹 **Recursive Calls vs. Flights**

Shows search-space explosion.

🔹 **Gantt Chart**

Visual representation of flight assignments across crew members.

🚀 **How to Run**

**Install required libraries:**

pip install matplotlib memory_profiler


**Run the Jupyter Notebook:**

jupyter notebook crew_scheduling.ipynb


Explore:

Flight assignment

Gantt chart

Performance graphs

🧠 **Complexity Analysis**

Backtracking complexity → Exponential

**Worst-case:**

𝑂
(
𝑘
𝑛
)
O(k
n
)

where

n = number of flights

k = number of crew members

This explains the exponential rise in execution graphs.

📝 **Conclusion**

This project demonstrates:

How real-world flight scheduling maps to NP-hard problems

Why exponential algorithms are infeasible at large scale

How backtracking works for constraint satisfaction

How profiling reveals computational limits

How visualization helps interpret solutions
