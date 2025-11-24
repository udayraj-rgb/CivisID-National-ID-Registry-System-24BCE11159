# CivisID: National ID Registry System

**CivisID** is a Java-based Command Line Interface (CLI) application designed to simulate the backend workflows of a real-world national citizen registration and verification system. Built with a focus on accuracy, scalability, security, data integrity, and persistent storage, it goes far beyond traditional console-based programs.

##  Project Overview

While basic Java applications lose data upon exit, **CivisID ensures permanent storage** using CSV-based data files, making all records easily exportable, readable, and compatible with tools like Excel, Google Sheets, and government data platforms.

### Core Objectives
CivisID is designed to help the government maintain a centralized citizen database, enabling authorities to know essential details about each citizen—such as identity, age, address, phone number, and email—ensuring consistent and accurate record-keeping across departments.

Each citizen is assigned a unique **CivisID Number**, which is used to:
* Verify the authenticity of the user.
* Prevent duplicate registrations.
* Ensure secure access and identity validation.
* Track updates made by the citizen or the authorities.

### Empowering E-Governance
The application collects **Email IDs** and **Phone Numbers**, enabling the system to:
* Deliver government schemes, subsidies, and welfare updates.
* Send important notifications, emergency alerts, and reminders.
* Maintain direct communication between public departments and citizens.

Overall, CivisID replicates the fundamental features of national ID systems (similar to Aadhaar, SSN, etc.) by providing secure registration, validation, monitoring, and data persistence—all from a lightweight and efficient Java CLI environment.

---

## Key Features

###  1. Dynamic & Context-Aware Relative Logic
The system intelligently adapts the registration flow based on **Gender** and **Marital Status**. This mirrors real government documentation patterns.

| Citizen Type | Relative Prompt |
| :--- | :--- |
| **Married Male** | Wife’s Name |
| **Married Female** | Husband’s Name |
| **Unmarried** | Father’s Name |

### 2. Secure 7-Digit Random National ID
Each citizen receives a **non-sequential, unpredictable 7-digit ID**. This increases anonymity and prevents ID guessing attacks.

###  3. Permanent CSV Data Storage
CivisID uses `citizens.csv` to store data persistently.
* ✔ Auto-creates CSV with headers if missing.
* ✔ Appends new data safely.
* ✔ Readable in Excel/Google Sheets.
* ✔ Follows structured, clean formatting.

###  4. Full CRUD Management
The administrator has full control over the registry:
* **Create:** Register new citizens.
* **Read:** Search by ID (Instant lookup).
* **Update:** Modify name, address, pincode, contact info.
* **Delete:** Remove unwanted/invalid records from the active session.

### 5. Comprehensive Data Capture
The system captures **15+ essential data points**:
* Full Name, Age, DOB, Gender
* Relative Name (Context-Aware)
* Address, Pincode, State
* Mother Tongue, Family Members
* ID Proof, National ID
* Phone, Email
* Registration Timestamp

---

## Tech Stack

| Component | Technology | Purpose |
| :--- | :--- | :--- |
| **Language** | Java (JDK 8+) | Secure, portable, enterprise-grade logic. |
| **Data Structure** | `HashMap<String, Citizen>` | **O(1)** fast retrieval of records during runtime. |
| **OOP** | Encapsulation | Protects data integrity via Getters/Setters. |
| **File I/O** | `FileWriter` | persistent CSV storage management. |
| **Error Handling** | `try-catch` | Prevents crashes on invalid input or file errors. |

---

## Project Structure

```text
National-ID-System/
│
├── Citizen.java        # Model class for citizen data (POJO)
├── FileHandler.java    # Handles CSV file creation & data writing
└── NationalIDApp.java  # Main controller (Menu, Scanner, Logic, CRUD)


