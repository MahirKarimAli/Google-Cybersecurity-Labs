# Google Cybersecurity Certificate - Lab: Navigating the Linux File System

## Introduction
As a cybersecurity analyst, efficiently navigating a Linux environment is an essential skill for investigating system activity, auditing user access, and reading security logs. In this lab, I practiced moving through a directory structure, inspecting directory contents, and analyzing files using the Linux command-line interface (CLI).

---
## Lab Reference Artifact
Below is the complete, error-free terminal session documenting the commands executed and the file outputs described above:

![Linux Terminal Session Walkthrough]<img width="831" height="763" alt="fdcf4e0e-2880-4ab2-8c61-77bed206ab3f" src="https://github.com/user-attachments/assets/0f1a2fc2-083d-41bd-a218-6f6c20dc1824" />

---

## Technical Walkthrough

### Task 1 & 2: Finding My Bearings and Exploring Subdirectories
I began the session by verifying my initial location in the system and checking the available files and directories.

* **Commands used:** `pwd`, `ls`, and `cd reports/`
* **Observation:** The `pwd` command confirmed my starting location was `/home/analyst`. Listing the directory contents revealed folders named `logs`, `projects`, `reports`, and `temp`. Moving into the `reports/` folder and running `ls` showed a subdirectory named `users`.

---

### Task 3: Auditing User Records
Next, I navigated deeper into the file hierarchy to locate and audit organizational user data.

* **Commands used:** `cd users/`, `ls`, and `cat Q1_added_users.txt`
* **Analysis Findings:** 
  By outputting the contents of `Q1_added_users.txt`, I answered key structural security audit questions:
  * **What department does the employee with the username `aezra` work in?** Human Resources.
  * **What is the `employee_id` of the user `mreed` in the Information Technology department?** 1104.

---

### Task 4: Inspecting Log Files
Finally, I jumped directly to the log folder using an absolute path to check system events for immediate warnings.

* **Commands used:** `cd /home/analyst/logs/`, `ls`, and `head server_logs.txt`
* **Log Analysis:** 
  Using `head` allowed me to view the first 10 entries of `server_logs.txt` instantly without cluttering the screen. Looking closely at the log output, I identified **three warning messages** regarding file storage limits and password expirations:
  1. `The file storage is 75% full`
  2. `The file storage is 90% full`
  3. `The current user’s password expires in 15 days`


## Conclusion
This lab provided practical experience with core Linux commands (`pwd`, `cd`, `ls`, `cat`, `head`). Running through the sequence perfectly demonstrated the efficiency of the command line. Navigating directory structures to check user file permissions or parse through server logs mirrors the foundational daily workflow of a Security Operations Center (SOC) analyst.
