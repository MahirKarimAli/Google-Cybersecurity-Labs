# Google Cybersecurity Certificate - Lab: Filtering Data with Grep and Pipes

## Introduction
In cybersecurity, analysts are routinely inundated with massive amounts of raw log and user data. Being able to quickly find specific indicators of compromise (IoCs) or track system modifications requires efficient filtering tools. In this lab, I leveraged the power of the `grep` command and command piping (`|`) to isolate critical security events and audit user data changes within a Linux file system.

---

## Technical Walkthrough

### Task 1: Searching for Error Messages in a Log File
Manually inspecting thousands of log entries during an investigation is inefficient. I used text filtering to target critical failures instantly.

* **Commands used:** `cd /home/analyst/logs/` and `grep error server_logs.txt`
* **Analysis Findings:** By running `grep`, the terminal filtered out everything except lines explicitly containing the string "error". I isolated exactly **six** distinct error entries, noting issues ranging from incorrect authentication attempts to unauthorized access events.

<img width="697" height="178" alt="ss 1" src="https://github.com/user-attachments/assets/39dad9f0-bf7f-493f-8370-985952c0f638" />

---

### Task 2: Finding Files Using Command Piping
When working with directories containing numerous records, combining commands using a pipe (`|`) allows an analyst to filter directory listings dynamically.

* **Commands used:** `ls | grep Q1` and `ls | grep access`
* **Observation:** Piping sends the standard output of `ls` directly into `grep` as its input. 
  * Filtering for "Q1" revealed **three** specific files (`Q1_access.txt`, `Q1_added_users.txt`, `Q1_deleted_users.txt`).
  * Filtering for "access" isolated **four** quarterly access log files (`Q1_access.txt` through `Q4_access.txt`).

<img width="632" height="207" alt="ss 2" src="https://github.com/user-attachments/assets/e9e05d95-99b4-441d-a6ce-334b60a440aa" />

---

### Task 3: In-Depth Content Searching for User Audits
For the final phase of the lab, I performed a content check inside the text files to view the contents of the full directory and audit specific user access modifications.

First, I displayed the full inventory of files available in the directory:
<img width="786" height="113" alt="ss 3" src="https://github.com/user-attachments/assets/e11b88a4-926b-4b1c-adde-87c7a675153d" />

Next, I targeted specific entries within those files using focused keywords:
* **Commands used:** `grep jhill Q2_deleted_users.txt` and `grep "Human Resources" Q4_added_users.txt`
* **Investigation Results:**
  * Searching for `jhill` in the Q2 deleted users file returned a positive match, confirming they were removed while working under the Sales department.
  * Searching for the multi-word string `"Human Resources"` in the Q4 added users file revealed that **two** employees (`sshah` and `msosa`) were added to the HR department in that quarter.

<img width="877" height="115" alt="ss 4" src="https://github.com/user-attachments/assets/dfcae92f-220d-4e4d-9e8a-a5af58e45e7c" />

---

## Conclusion
This lab highlighted how fundamental text filtering is to day-to-day security workflows. Mastering `grep` and command piping allows me to slice through data clutter efficiently, transforming massive amounts of raw text into actionable data points—a critical skill when performing live triage or parsing server logs during incident response.
