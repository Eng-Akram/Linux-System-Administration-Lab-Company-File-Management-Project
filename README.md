\# Linux System Administration Lab – Company File Management Project



\## 📌 Project Overview

This project simulates an enterprise-level file management environment built entirely from the Linux Command Line (CLI). The objective was to design a structured corporate workspace, manage file lifecycles, understand link behaviors under the hood, and optimize the shell environment for maximum administrative productivity.



\---



\## 🛠️ Technologies \& Tools Used

\* \*\*Operating System:\*\* Ubuntu Linux (via VMware Virtual Platform)

\* \*\*Shell:\*\* Bash (Bourne Again Shell)

\* \*\*Text Editor:\*\* Nano

\* \*\*Core Utilities:\*\* Linux CLI, `tree`, `ln`, `grep`, `alias`, `tar`, `file`



\---



\## 📁 Directory Architecture

The project simulates a corporate structure consisting of 7 directories and 11 files, structured hierarchically to organize departmental data (`HR`, `IT`, `Finance`, `Reports`, `Backups`).



You can see the generated directory tree structure in \*\*Screenshot 2026-06-27 150022.png\*\*.



\---



\## 🔍 Key Tasks \& Implemented Features



\### 1. File \& Directory Management

\* Built a complete corporate directory hierarchy using `mkdir`.

\* Managed files using `touch`, `cp` (copying data to backups), and `mv` (moving budget files into the Reports folder).

\* Utilized Wildcards (`\*`) for efficient bulk file classification (e.g., sorting `.txt` and `.pdf` files simultaneously).



\### 2. Deep Dive: Hard Links vs. Symbolic Links

\* Created a \*\*Hard Link\*\* (`HR/employees\_hardlink.txt`) pointing to the same inode as the source. 

\* Created a \*\*Symbolic (Soft) Link\*\* (`employees\_shortcut`) acting as a shortcut path.

\* \*\*Testing Resilience:\*\* Deleted the original source file (`rm HR/employees.txt`) to analyze the behavior:

&#x20; \* The \*\*Symbolic Link\*\* broke immediately (dangling link).

&#x20; \* The \*\*Hard Link\*\* remained perfectly intact and preserved the file content because the underlying inode link count was still active.

&#x20; \* Checked inode details using `ls -li HR` as demonstrated in \*\*Screenshot 2026-06-27 150144.png\*\*.



\### 3. Shell Customization \& Automation

\* Configured persistent custom aliases within the `\~/.bashrc` file to optimize administrative efficiency:

&#x20; \* `proj`: Quick navigation shortcut directly into the project directory (`cd \~/company\_project`).

&#x20; \* `11`: Custom list format wrapper (`ls -lah`).

&#x20; \* `cls`: Simplified screen clearing mechanism.

\* Inspected standard shell configurations using the `alias` command as recorded in \*\*Screenshot 2026-06-27 150350.png\*\*.



\### 4. Linux Help \& Terminal Reporting

\* Extensively used documentation tools (`man`, `help`, `whatis`) to inspect command syntaxes.

\* Maintained productivity tracking by auditing command history via `history | grep cp`.

\* Generated a structured, formal project summary file (`project\_report.txt`) completely inside the terminal using the `nano` editor.



\---



\## 📈 Skills Demonstrated

\* \*\*System Administration Fundamentals:\*\* Understanding structure, permissions, and environment setup.

\* \*\*Linux File System Architecture:\*\* Managing data layout, Inodes, and system links.

\* \*\*Bash Productivity:\*\* Scripting shortcuts, terminal customization, and utilizing configuration files (`.bashrc`).

\* \*\*Troubleshooting:\*\* Diagnosing broken paths and tracking execution logs via execution command histories.



\---



\## 📸 Terminal Snapshots \& Execution Proofs



Here is the sequential log of the terminal execution for this lab session:

\* <p align="center">
  <img src="Screenshot 2026-06-27 150236.png" alt="Topology" width="800">
</p>
Comprehensive command history showing folder generation, file text creation (`cat`/`tac`), and file sorting.

\* !\[Alternative Text](Screenshot 2026-06-27 150258.png): Command history documenting link breaking experiments, wildcard lookups (`ls \*.txt`), and internal documentation manual checks (`man ls`).

\* !\[Alternative Text](Screenshot 2026-06-27 150315.png): Setup history detailing package updates (`apt install tree`) and navigating system directories.

\* !\[Alternative Text](Screenshot 2026-06-27 150434.png): Output of the final `project\_report.txt` file printed on the screen using the `cat` command.



\---

\*Developed by Akram Hesham | June 27, 2026\*

