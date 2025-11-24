🏛️ CivisID: National ID Registry System

CivisID is a Java-based CLI application designed to simulate the backend workflows of a real-world national citizen registration system. It emphasizes accuracy, scalability, data integrity, and persistence, making it far more capable than traditional console programs.

Unlike basic applications that lose data after exiting, CivisID stores all citizens permanently using CSV files, making data portable, readable, and compatible with Excel, Google Sheets, and other tools.

🚀 Key Features
✅ 1. Dynamic & Context-Aware Relative Logic

The system intelligently adapts based on Gender and Marital Status:

Citizen Type	Relative Prompt
Married Male	Wife’s Name
Married Female	Husband’s Name
Unmarried	Father’s Name

This mirrors real government documentation patterns.

✅ 2. Secure 7-Digit Random National ID

Each citizen receives a non-sequential, unpredictable 7-digit ID, increasing anonymity and security.

✅ 3. Permanent CSV Data Storage

CivisID uses citizens.csv to store data persistently.

✔ Auto-creates CSV with headers
✔ Appends new data safely
✔ Readable in Excel/Sheets
✔ Follows structured, clean formatting

✅ 4. Full CRUD Management

The admin can:

Create new citizens

Read/Search by ID

Update name, address, pincode, etc.

Delete unwanted/invalid records

✅ 5. Comprehensive Data Capture

15+ fields are collected:

Full Name

Age

DOB

Gender

Relative Name

Address

Pincode

State

Mother Tongue

Family Members

ID Proof

Phone

Email

National ID

Registration Timestamp

🛠️ Tech Stack
Component	Technology	Purpose
Language	Java (JDK 8+)	Secure, portable, enterprise-grade
Data Structure	HashMap<String, Citizen>	O(1) fast retrieval of records
OOP	Encapsulation	Protects data integrity
File I/O	FileWriter	Persistent CSV storage
Error Handling	try-catch	Prevents crashes and invalid data
📂 Project Structure (MVC-Style Architecture)
📦 National-ID-System
 ┣ 📜 Citizen.java         # MODEL - defines citizen blueprint (fields + getters/setters)
 ┣ 📜 FileHandler.java     # UTILITY - handles CSV writing & file checks
 ┗ 📜 NationalIDApp.java   # CONTROLLER - main logic, menu, interaction flow

⚙️ How to Run
1️⃣ Clone the Repository
git clone https://github.com/YourUsername/CivisID.git
cd CivisID

2️⃣ Compile All Java Files
javac *.java

3️⃣ Run the Application
java NationalIDApp

📊 Sample CSV Output

The app generates a structured citizens.csv file like:

NationalID	Name	Age	Gender	Relation	Phone	Email	Address	DateRegistered
7829103	Rahul Sharma	34	Male	Wife: Priya	9876543210	rahul@gov.in
	12 MG Road	2025/11/24
1928374	Aditi Rao	29	Female	Father: Raj	9123456789	aditi@gov.in
	45 Indiranagar	2025/11/24
🔮 Future Enhancements

JavaFX/Swing GUI for a modern desktop interface

MySQL/PostgreSQL with JDBC for large-scale government usage

Biometric Hashing (SHA-256 simulation)

Cloud Sync via REST APIs (Firebase/AWS)

Advanced Search & Filtering

👨‍💻 Developed By

[Udayraj Patil]
National ID System — Educational Prototype for e-Governance Concepts
