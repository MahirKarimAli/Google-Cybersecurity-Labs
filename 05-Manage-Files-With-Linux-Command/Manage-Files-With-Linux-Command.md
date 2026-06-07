# Google Cybersecurity Certificate - Lab: File Organization and Text Editing in Linux

## Introduction
Cybersecurity analysts must be proficient not only in auditing file systems but also in actively managing them. Whether configuring security application profiles, isolating suspicious files, or maintaining active incident logs, file system manipulation is a core operational capability. In this lab, I practiced creating and removing directories, moving and deleting files, and utilizing the `nano` command-line text editor to document system tasks.

---

## Technical Walkthrough

### 1. Directory Hygiene (Creating and Removing Environments)
Maintaining a secure and clean workspace minimizes the risk of system clutter and untracked files. I began by initializing a dedicated directory for logging metadata and removing an unneeded temporary directory.

* **Commands used:** `mkdir logs`, `rmdir temp`, and `ls`
* **Workflow:** 
  First, I generated a new `logs` subdirectory and used `ls` to verify its placement alongside existing system folders (`ss1.png`). Following that, I cleanly targeted and deleted an obsolete `temp` folder using `rmdir`, running a subsequent check to confirm a streamlined environment (`ss2.png`).

<img width="396" height="73" alt="ss1" src="https://github.com/user-attachments/assets/6f018c90-845e-4118-90f2-96ac75f33483" />
<img width="413" height="67" alt="ss2" src="https://github.com/user-attachments/assets/cd5453d5-679b-40c0-938e-ef3dc19159db" />

---

### 2. Data Relocation and Asset Destruction
Security documentation needs to reside in proper authorized repositories, and stale notes containing sensitive data should be permanently disposed of when no longer needed.

* **Commands used:** `cd notes/`, `mv Q3patches.txt /home/analyst/reports/`, `rm tempnotes.txt`, and `ls`
* **Workflow:**
  I stepped into the `notes/` directory and transferred a finalized patch report (`Q3patches.txt`) straight to the `reports/` folder using `mv`. An immediate check verified that all three quarterly patch logs were neatly Consolidated (`ss3.png`). Next, I returned to the parent space and completely purged an unused helper file named `tempnotes.txt` using `rm`, leaving the folder pristine and vacant (`ss4.png`).

<img width="786" height="206" alt="ss3" src="https://github.com/user-attachments/assets/7c376b86-f244-4e26-ac34-af43d360a45b" />
<img width="553" height="137" alt="ss4" src="https://github.com/user-attachments/assets/ae0626e8-f5ee-4b10-b8c8-0a1e0fffe8d0" />

---

### 3. File Initialization and Interactive Editing via Nano
To close out the operational checklist, I practiced setting up an empty file tracking asset and using a native text editor to document my system updates directly through the shell interface.

* **Commands used:** `touch tasks.txt`, `nano tasks.txt`, and `cat tasks.txt`
* **Workflow:**
  I used `touch` to quickly initialize a blank file named `tasks.txt` inside the empty notes workspace (`ss5.png`). From there, I launched the `nano` text editor terminal wrapper (`ss6.png`), populating it with an operational summary tracking my exact administrative accomplishments (`ss7.png`).

<img width="512" height="70" alt="ss5" src="https://github.com/user-attachments/assets/2e60c643-7197-48ee-8da8-c0bad9f1a316" />
<img width="562" height="26" alt="ss6" src="https://github.com/user-attachments/assets/cc7fb250-448f-4fdd-a32a-58fae120e183" />
<img width="877" height="132" alt="ss7" src="https://github.com/user-attachments/assets/8fa800f1-dbff-4c27-bf81-ade554c085f2" />

To exit and preserve the modifications safely within the terminal environment, I executed the interactive buffer sequence: 
1. Triggered the exit routine with **`Ctrl + X`**.
2. Saved the modified buffer by typing **`Y`** (`ss8.png`).
3. Confirmed the output target as `tasks.txt` with **`Enter`** (`ss9.png`).

<img width="880" height="102" alt="ss8" src="https://github.com/user-attachments/assets/3565ef7d-df9a-4644-a53f-2e8dec556e95" />
<img width="876" height="78" alt="ss9" src="https://github.com/user-attachments/assets/e1e68a45-cdda-40ed-8138-b84e62a270b7" />

Finally, I verified that the document was cleanly compiled and stored onto disk by reading out its contents using `cat` (`ss10.png`).

<img width="575" height="128" alt="ss10" src="https://github.com/user-attachments/assets/1080269c-ad58-464c-a6cb-bd8a70b7b743" />

---

## Conclusion
This lab simulated vital data management habits crucial for modern security practitioners. Safely adjusting directory structures, executing precise relative and absolute file transfers, and editing configurations directly via `nano` are fundamental mechanics I will rely on daily when adjusting tool permissions, rotating operational logs, or building rapid incident response timelines.
