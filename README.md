CivisID: National ID Registry System

CivisID is a Java-based CLI application designed to simulate the backend workflows of a real-world national citizen registration and verification system. Built with a focus on accuracy, scalability, security, data integrity, and persistent storage, it goes far beyond traditional console-based programs.

While basic Java programs lose data after exiting, CivisID ensures permanent storage through CSV files, making records exportable, readable, and compatible with Excel, Google Sheets, and government platforms.

This system is designed to help the government maintain a centralized citizen registry, enabling authorities to store and verify essential details such as identity, age, address, phone number, and email—ensuring consistent, unified record-keeping.

Each citizen receives a unique CivisID Number, used to:

Verify authenticity

Prevent duplicate registrations

Ensure secure identity validation

Track modifications and updates

The system also collects phone numbers and emails, allowing:

Delivery of government schemes and subsidy updates

Emergency alerts and important notifications

Direct communication with citizens

Overall, CivisID replicates core features found in national ID systems (similar to Aadhaar, SSN, etc.), providing secure registration, verification, monitoring, and persistent storage in a lightweight Java console application.

Key Features
1. Dynamic & Context-Aware Relative Logic

The system intelligently adjusts relative prompts based on gender and marital status:

Citizen Type	Relative Prompt
Married Male	Wife’s Name
Married Female	Husband’s Name
Unmarried	Father’s Name

This mimics real documentation practices in government systems.

2. Secure 7-Digit Auto-Generated National ID

Random, non-sequential

Hard to predict

Enhances anonymity and data security

3. Permanent CSV-Based Data Storage

The file citizens.csv stores all information permanently.

Automatically creates file and headers

Appends new entries safely

Structured formatting compatible with Excel/Sheets

Ensures long-term data integrity

4. Full CRUD Operations (Admin Panel)

Create new citizens

Read/Search citizens by ID

Update name, address, phone, pincode, etc.

Delete incorrect or unwanted records

5. Comprehensive Data Collection

The system captures over 15 demographic fields:

Name

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

Tech Stack
Component	Technology Used	Purpose
Language	Java (JDK 8+)	Secure, portable, enterprise-grade
Data Structure	HashMap<String, Citizen>	O(1) fast lookup and retrieval
OOP Concepts	Encapsulation	Protects and organizes data
File Storage	FileWriter / BufferedWriter	Persistent CSV record management
Error Handling	try-catch	Prevents crashes and invalid input
Project Structure
National-ID-System/
│
├── Citizen.java          # Model class (POJO)
├── FileHandler.java      # CSV creation, reading, and writing
└── NationalIDApp.java    # Main controller (menu + CRUD + storage)

How to Run
1. Clone the Repository
https://github.com/udayraj-rgb/CivisID-National-ID-Registry-System-24BCE11159.git

2. Compile All Java Files
javac *.java

3. Run the Application
java NationalIDApp

Sample CSV Output
NationalID, Name, Age, Gender, Relation, Phone, Email
7829103, Rahul Sharma, 34, Male, Wife: Priya, 9876543210, rahul@gov.in
1928374, Aditi Rao, 29, Female, Father: Raj, 9123456789, aditi@gov.in

Future Enhancements

GUI using JavaFX/Swing

MySQL/PostgreSQL integration using JDBC

Biometric hashing (SHA-256 simulation)

Cloud synchronization via REST APIs

Advanced search, filtering & analytics

Developed By

Udayraj Patil
National ID System — Educational Prototype for e-Governance Concepts
