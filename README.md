# Project Report: Offline Fingerprint-Based Classroom Attendance System

## 🧠 Problem

In many classrooms, attendance is taken either at the **start** or at the **end** of the class. This creates a problem because:

- If it’s taken at the beginning, some students **leave early**.
- If it’s taken at the end, some students **come late** just to be marked present.

---

## ✅ Solution

To solve this, we are creating an **offline attendance system** that uses a **mobile fingerprint scanner** and a **laptop**. Students will scan their fingerprints **both when they enter and when they leave** the classroom.

The system will record the **time of both scans** and **calculate how long each student stayed**. This way, only students who actually attend **most of the class** will be marked present.

---

## 🎯 Objective

- Develop an effective solution for attendance issues in a class.
- Mark student attendance.
- Track **entry and exit times**.
- Calculate the **total time** each student spends in the classroom.

---

## 🛠️ Technologies and Tools Used

### 1. Mobile Fingerprint Scanner
- **Purpose:** Authenticate a student’s fingerprint and send an attendance signal.
- **Function:** Once a fingerprint is authenticated, the app sends a **timestamp** and **student identifier** to the laptop.

---

### 2. Communication Method
- **USB Tethering**

---

### 3. Laptop Backend
- **Language:** Python  
- **Framework:** Flask (chosen for being lightweight)

**Purpose:**
- Receive scan data from mobile.
- Log timestamp and student details.
- Determine entry/exit and calculate duration.

---

### 4. Data Storage

#### Option 1: CSV File
- Simple **Comma-Separated Values** file for logging.

#### Option 2: SQLite Database
- Structured and queryable data storage.

**Suggested Tables:**

- `students(student_id, name)`
- `attendance_logs(log_id, student_id, action, timestamp)`
- `sessions(session_id, student_id, entry_time, exit_time, duration)`

---

### 5. UI

- **Technology:** Flask + HTML/CSS/JavaScript

**Purpose:**
- Export attendance (can be viewed after class).
- View and filter student history (all logs for student movement for a specific class).

---
