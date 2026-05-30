# Lab: Managing Software Packages in Linux

## Project Overview
This lab is part of the **Google Cybersecurity Professional Certificate**. The objective was to practice software package management on a Linux distribution using the Advanced Package Tool (`apt`). I successfully managed installations, verified software status, handled uninstallation, and resolved package states using the command-line interface (CLI).

## Skills Demonstrated
* Linux Command Line Interface (CLI)
* Package Management (`apt`)
* Network Security Tool Deployment (`tcpdump` & `suricata`)
* Listing installed Packages (`list --installed`)

---

## Lab Execution & Evidence

### Step 1: Initial Software Verification
I began by launching `suricata` to verify its initial installation status on the system.
* **Command Used:** `suricata` (or tool execution command)
* **Evidence:** <img width="883" height="592" alt="ss1" src="https://github.com/user-attachments/assets/f9cf9cc8-f402-4854-abc9-4d57f9da21a2" />

### Step 2: Removing a Package
To practice uninstallation and clean up system resources, I removed the `suricata` package.
* **Command Used:** `sudo apt remove suricata`
* **Evidence:** <img width="883" height="757" alt="ss2" src="https://github.com/user-attachments/assets/6f78cf94-e35e-4078-bf90-ae77a21824bf" />

### Step 3: Installing a New Network Tool
Next, I installed `tcpdump`, a critical command-line packet analyzer used for network security monitoring.
* **Command Used:** `sudo apt install tcpdump`
* **Evidence:** <img width="883" height="692" alt="ss3" src="https://github.com/user-attachments/assets/319a7381-bffa-4ee3-a697-df0cb4ba4ce5" />

### Step 4: System Auditing (First Pass)
I generated a complete list of all installed packages on the system to prepare for validation.
* **Command Used:** `apt list --installed`
* **Evidence:** <img width="883" height="257" alt="ss4" src="https://github.com/user-attachments/assets/b9b27139-76be-44c1-8951-49d01c26aca7" />

### Step 5: Verifying Tcpdump Installation
I filtered the package list to explicitly confirm that `tcpdump` was successfully active on the system.
* **Command Used:** `apt list --installed`
* **Evidence:** <img width="882" height="300" alt="ss5" src="https://github.com/user-attachments/assets/2b0f266e-d430-493b-a58e-5737b041336e" />


### Step 6: Reinstalling Suricata
To simulate a multi-tool security environment, I reinstalled the `suricata` intrusion detection system package.
* **Command Used:** `sudo apt install suricata`
* **Evidence:** <img width="882" height="600" alt="ss6" src="https://github.com/user-attachments/assets/69930b5c-e8f8-4678-85e3-d5df3f777aa2" />


### Step 7: System Auditing (Second Pass)
I pulled the updated list of installed packages to ensure the system configuration changed correctly.
* **Command Used:** `apt list --installed`
* **Evidence:** <img width="882" height="325" alt="ss7" src="https://github.com/user-attachments/assets/4fe05475-820e-42df-b98e-8e27f7b88ceb" />


### Step 8: Final Environment Validation
I ran a final check confirming that both `tcpdump` and `suricata` were concurrently installed and ready for security operations.
* **Command Used:** `apt list --installed`
* **Evidence:** <img width="883" height="298" alt="ss8" src="https://github.com/user-attachments/assets/3b1d2f00-7fd7-46ed-93da-3a1113d745a1" />


---

## Key Takeaways
1. **Repository Management:** Learned how `apt` syncs with remote repositories to fetch and deploy stable security tools.
2. **System Auditing:** Understanding how to generate and read the complete `apt list --installed` output is essential for security analysts to manually verify if required tools are present or unauthorized software is running.
3. **Environment Control:** Gained hands-on experience installing, removing, and reinstating network sniffers (`tcpdump`) and signature-based detection systems (`suricata`) on a Linux workstation.
