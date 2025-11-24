##Project Statement: CivisID National Registry

##1. Problem Statement In many developing regions, citizen registration remains a manual, paper-based process. This leads to several critical issues:

Data Redundancy & Errors: Illegible handwriting and duplicate entries are common.

Inefficient Retrieval: Searching for a citizen's record among thousands of physical files is time-consuming and prone to failure.

Lack of Standardization: Different regions may capture different data points, making national-level analysis difficult.

Data Vulnerability: Physical records are susceptible to damage from fire, water, or misplacement.

Social Context Gap: Static forms often fail to capture culturally relevant relationship data accurately (e.g., specifically noting a husband's name versus a father's name based on marital status).

There is a clear need for a digital, standardized, and intelligent system to digitize citizen records, ensuring data integrity, quick access, and context-aware data capture.

##2. Scope of the Project This project aims to develop a Java-based Command Line Interface (CLI) application designed to simulate the backend logic of a national identity registry.

In-Scope:

Digital Registration: A structured CLI form to capture demographic, contact, and biometric-proof details.

Intelligent Logic: Implementing conditional logic to determine the appropriate relative's name (Wife/Husband/Father) based on gender and marital status inputs.

Unique Identification: Automated generation of a random, non-colliding 7-digit National ID for every new registrant.

Data Persistence: Saving all registered records permanently into a structured CSV (Comma Separated Values) file for external audit and analysis.

In-Memory Search: Instantaneous lookup of citizen details using their 7-digit ID during the active application session.

Basic CRUD Operations: Allowing for the registration (Create), searching (Read), updating of specific fields (Update), and soft-deletion (Delete) of records from the active session.

Out-of-Scope:

Graphical User Interface (GUI): The project is limited to a text-based console interface.

Real Database Integration: A full RDBMS (like MySQL or Oracle) is not used; data is managed via CSV files.

Biometric Hardware Integration: The system captures an ID proof number but does not interface with actual fingerprint or iris scanners.

Network/Cloud Connectivity: The application runs locally on a single machine and does not synchronize data across a network.

##3. Target Users

Government Registrars & Clerks: The primary users who will sit at registration desks, interviewing citizens and entering their data into the system. They require a simple, text-driven interface that guides them through the process rapidly.

System Administrators / Auditors: Officials who need to access the backend CSV files to generate reports, perform population analysis using spreadsheet software, or review historical registration data.

###4. High-Level Features

Smart Data Capture: Context-aware prompts that change based on user input (e.g., asking for "Spouse Name" only if married).

Auto-ID Generation: Creation of a unique 7-digit identifier for each citizen, ensuring no duplicates within the system logic.

Persistent Storage: All successful registrations are automatically appended to a citizens.csv file, creating a permanent, exportable record.

Instant Search: Utilizes an in-memory HashMap to provide immediate retrieval of citizen records by querying their unique ID.

Record Management: Provides menu-driven options to update mutable details (like phone number or address) and remove records from active processing.

Audit Trail: Every record in the CSV file is timestamped to indicate the exact date and time of registration.
