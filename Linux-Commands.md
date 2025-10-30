# Week 2: Linux Command Line Mastery (Fundamentals & Security)

This week, I focused on becoming proficient in the Linux command line (Terminal) within my isolated Kali VM, which is essential for all security tooling and administration.

## Essential Commands Practiced

| Command | Purpose | Job Relevance |
| :--- | :--- | :--- |
| **`pwd`** | Prints the current folder location. | Navigating server environments. |
| **`ls -l`** | Lists files with detailed permissions. | **Critical for auditing** (seeing who can access what). |
| **`cd`** | Changes the current directory. | Moving through file systems quickly. |
| **`ip a`** | Shows the network (IP) address. | **Crucial for initial triage** and network config validation. |
| **`mkdir`** / **`touch`** | Creates new folders/empty files. | Organizing tool outputs and logs. |
| **`cat`** / **`echo`** | Reads the contents of a file. | Viewing configuration files and logs. |
| **`cp`** / **`rm`** | Copies and deletes files. | Basic file management (used with extreme caution). |

## Key Security Concept: File Permissions (`chmod`)

I practiced securing files using the **Principle of Least Privilege**.

| Command Executed | Permission Breakdown | Result |
| :--- | :--- | :--- |
| **`touch secret.txt`** | - | Creates a new file. |
| **`chmod 700 secret.txt`** | `7` (rwx) for **Owner**; `0` (---) for **Group**; `0` (---) for **Other**. | **Locked the file:** Only I, the owner, can read, write, or execute this file. This prevents other users (or processes running as another user) from accessing sensitive data, which is a core defense mechanism. |
