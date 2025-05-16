# 🖨️ FM-Printer Setup Guide

Follow the steps below to set up the FM-Printer agent on your system:

---

### 📥 Step 1: Download and Extract
- [📦 Click here to download the ZIP file](https://github.com/SunnyAryaFM/FM-Printer/raw/refs/heads/main/printer.zip)
- Extract the contents to:  
  `C:\Users\Sunny\Downloads\out`

---

### ⚙️ Step 2: Create a Task in Task Scheduler
1. Press `Win + S`, search for **Task Scheduler**, and open it.
2. Click **Create Task** on the right panel.
3. In the **General** tab:
   - Give the task a name, e.g., `Printer Agent`.
   - Check the option **Run with highest privileges** (recommended).
4. In the **Triggers** tab:
   - Click **New**.
   - Set **Begin the task** to **At startup**.
   - Click **OK**.
5. In the **Actions** tab:
   - Click **New**.
   - Set **Action** to **Start a program**.
   - In **Program/script**, enter:
     ```
     powershell
     ```
   - In **Add arguments**, enter:
     ```
     -ExecutionPolicy Bypass -File "C:\Users\Sunny\Downloads\out\printer.ps1"
     ```
   - Click **OK**.

---

### 🔄 Step 3: Restart Your System
- After restarting, please **wait for 5 minutes** to allow the printer agent to initialize.

---

### ✅ Step 4: Verify It’s Working
- Open a browser and visit:  
  [http://localhost:4040/inspect/http](http://localhost:4040/inspect/http)  
  If the page loads, the printer agent is working correctly!

---
