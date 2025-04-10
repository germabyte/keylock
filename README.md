# Keylock

## 1. Introduction and Purpose

**Keylock** is a Windows-only utility that **temporarily disables all keyboard input** by locking the keyboard. The program remains active until the user performs a specific unlock gesture: pressing the spacebar five times in rapid succession (within one second). Once this condition is met, the program terminates itself and forcibly closes related processes.

### Purpose & Problem Statement

This script addresses the need for **temporarily disabling keyboard input** for privacy, focus, or security purposes. It can be particularly useful in situations where input should be disabled temporarily — for example, during a presentation, when leaving a workstation unattended briefly, or to prevent unintended key presses during critical processes.

### Value Proposition

- Simple activation: just run the script.
- Quick emergency unlock: press the spacebar five times quickly.
- No complex setup or configuration.
- Useful for parental control, kiosk environments, or secure workstations.

---

## 2. Dependencies (Required Software/Libraries)

This script requires the following external components:

### ✅ Python 3.x
- **Description:** The primary runtime environment required to execute the script.
- **Install:** [https://www.python.org/downloads](https://www.python.org/downloads)

### ✅ `pynput` Library
- **Description:** Enables the script to listen for keyboard inputs in the background.
- **Install Command:**
  ```bash
  pip install pynput
  ```

> ⚠️ **Note:** This script is **designed exclusively for Windows operating systems** due to its use of Windows-specific libraries like `ctypes.windll`.

---

## 3. Getting Started (Installation & Execution)

### Step-by-Step Instructions:

#### 1. Download the Repository
- Click the green "**<> Code**" button on the repository page.
- Select "**Download ZIP**".
- Extract the ZIP file to a location of your choice.

#### 2. Install Required Library
Open a terminal (Command Prompt) and run:
```bash
pip install pynput
```

#### 3. Run the Script
1. Press `Windows + R`, type `cmd`, and hit Enter to open the Command Prompt.
2. Navigate to the extracted folder using the `cd` command. For example:
   ```bash
   cd C:\Users\YourName\Downloads\keylock-main
   ```
3. Run the script using:
   ```bash
   python keylock.py
   ```

> 🔐 You will be prompted for **administrator permissions**, which are required to lock keyboard input.

---

## 4. User Guide (How to Effectively Use the Program)

### 🟢 Starting the Program
- Once launched, the script immediately locks the keyboard.
- You will see a message:  
  _“Press the spacebar 5 times rapidly to terminate the script and close all windows.”_

### 🔴 Unlocking the Keyboard / Stopping the Program
- Press the **spacebar 5 times within 1 second**.
- The script will:
  - Unlock the keyboard.
  - Terminate itself.
  - Attempt to close the terminal window and associated Python processes.

### 🛠 Configuration or Settings
- No configuration is needed.
- Behavior is fixed and hard-coded:
  - Unlock combo: 5 spacebar presses within 1 second.
  - Only works on Windows systems with administrator rights.

---

## 5. Use Cases and Real-World Examples

### ✅ Use Case 1: Parental Control
**Scenario:** A parent wants to temporarily disable keyboard input while their child is watching a video on the computer.  
**Action:** The parent runs the script to lock the keyboard.  
**Result:** The child cannot press any keys until the parent unlocks it with the spacebar combo.

### ✅ Use Case 2: Kiosk Mode Security
**Scenario:** A kiosk terminal must prevent users from pressing keys except via touchscreen.  
**Action:** The admin runs the script in the background on Windows.  
**Result:** The keyboard is disabled, improving kiosk security.

### ✅ Use Case 3: Focus Aid During Presentations
**Scenario:** A presenter wants to prevent accidental key presses while demonstrating something on screen.  
**Action:** Before beginning, the presenter runs the script.  
**Result:** Keyboard is locked, ensuring focus remains on content until unlocked manually.

---

## 6. Disclaimer & Important Notices

- This repository and its contents may be updated at any time without notice.
- Such updates may render parts of this README obsolete.
- No commitment is made to maintain or update this README to reflect future changes.
- The provided code is delivered **"as-is"**, with **no guarantees**—explicit or implied—regarding functionality, reliability, compatibility, or correctness.
- **Use at your own risk.**
