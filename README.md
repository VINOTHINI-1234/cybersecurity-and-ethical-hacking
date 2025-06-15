# cybersecurity-and-ethical-hacking
FILE INTEGRITY  CHECKER USING PYTHON


---

## 📌 Overview

The **File Integrity Checker** is a simple yet effective Python tool that uses **SHA-512** hashing to monitor the integrity of files in a directory. It helps detect:

- 🟡 **Newly added files**
- 🔴 **Modified files**
- 🟣 **Deleted files**
- 🟢 **Unchanged files**

By comparing current file hashes with a saved baseline, it ensures your files haven’t been tampered with or unintentionally altered.

---

## 🔍 Key Features

- ✅ Generate SHA-512 hash baseline of all files in a folder
- ✅ Detect changes by comparing current hashes to the baseline
- ✅ Logs results to `integrity_log.txt` for future auditing
- ✅ Uses **`colorama`** to color-code file status in terminal output

---

## 🛠️ Installation & Setup
✅ Prerequisites
- Python 3.x installed

Required Python modules:
- hashlib (standard library)
- colorama (install via pip)

---

## 📁 Folder Structure
File-Integrity-Checker/
- Files/                    # Folder to monitor
 │Subfolder/            # Nested files supported
- file_integrity_checker.py # Main Python script
- baseline.txt              # Stores SHA-512 hashes (auto-generated)
- integrity_log.txt         # Logs detected changes (auto-generated)
- Files/                    -># Folder to monitor
 │Subfolder/                -># Nested files supported
- file_integrity_checker.py -># Main Python script
- baseline.txt              -># Stores SHA-512 hashes (auto-generated)
- integrity_log.txt         -># Logs detected changes (auto-generated)

--- 

## ⚙️ Usage

**Step 1: Prepare Your Files** 
- Place the files or folders you want to monitor inside the Files/ directory.
Example: **File-Integrity-Checker/Files/ your_files_here.txt**

**Step 2: Create Supporting Files** 
- These files will be automatically created after the program runs:
1. **baseline.txt:** Stores original hash values (with comment headers).
2. **integrity_log.txt:** Logs any changes (added, modified, or deleted files)..

**Step 3: Run the Program** 
- Open a terminal and execute: **python file_integrity_checker.py**

**Step 4: Choose an Option** 
- After running the script, you’ll see: Choose an option: 1. Generate baseline 2. Check file integrity 3. Exit
1. Option 1: Generate Baseline (First Time Setup) - Use this option only once to create a reference (baseline.txt) of your files. This saves the hash of each file for comparison.
2. Option 2: Check Integrity (Subsequent Runs) - Use this to check if files were: Unchanged, Modified, New, Deleted.
3. Option 3: Exit

---
