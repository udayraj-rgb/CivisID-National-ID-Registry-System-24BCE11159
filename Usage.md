📘 Usage Guide – CivisID: National ID Registry System

by [Your Name] Department of Computer Science & Engineering

This guide explains how to set up, run, and use the CivisID application to manage citizen records efficiently.

🔧 Prerequisites

Before running this project, ensure the following are installed on your system:

Java SE 8+ (JDK 8, 11, 17, or 21)

Verify installation: java -version

Git (to clone the repository)

Text Editor/IDE: VS Code, IntelliJ IDEA, or Eclipse (Optional)

▶ Setup & Run

1. Clone the Repository

git clone [https://github.com/YourUsername/CivisID.git](https://github.com/YourUsername/CivisID.git)
cd CivisID


2. Compile the Source Code

Open your terminal/command prompt in the project folder and run:

javac *.java


3. Run the Program

Start the application using the main controller class:

java NationalIDApp


📑 CLI Menu Overview

When you run the program, you will see the following interactive menu:

=== NATIONAL ID REGISTRY SYSTEM (CSV) ===

--- MAIN MENU ---
1. Register New Citizen
2. Search Citizen by ID
3. Update Citizen Details
4. Delete Citizen
5. List All Registered Citizens
6. Exit
Enter Choice:


🔹 Functionalities & Usage

1️⃣ Register New Citizen

The system captures comprehensive demographic details.

Smart Relative Logic:

If Male & Married → Asks for Wife's Name.

If Female & Married → Asks for Husband's Name.

Otherwise → Asks for Father's Name.

Auto-ID: Generates a unique 7-digit National ID automatically.

Verification: Captures ID Proof Number (e.g., Old Voter ID) to verify authenticity.

2️⃣ Search Citizen by ID

Enter the 7-digit National ID to instantly retrieve details.

Displays Name, Relative Name, Contact Info (Phone/Email), and Address.

Note: Search works instantly from RAM (Memory).

3️⃣ Update Citizen Details

Allows correction of specific fields if data was entered incorrectly:

Name

Address

Phone Number

Select the field you wish to modify and enter the new value.

4️⃣ Delete Citizen

Removes a citizen from the Active Registry (RAM).

Note: The historical record remains in the CSV file for audit purposes, but the ID will no longer be searchable in the current session.

5️⃣ List All Registered Citizens

Prints a summary list of all citizens currently loaded in the active session.

6️⃣ Exit

Safely closes the application.

Ensures all file streams are closed.

📂 Data & Storage Files

The system uses a CSV (Comma Separated Values) file for permanent storage. This ensures data portability to government-standard tools like Excel.

citizens.csv

Location: Root project folder (automatically created after first registration).

Format:
NationalID, Name, Age, DOB, Gender, MaritalStatus, Relation, Phone, Email, Address, Pincode, State, MotherTongue, FamilyMembers, IDProof, DateRegistered

Usage:

The program Appends new records to this file.

If the file is missing, the program automatically creates it and writes the Header Row.

Tip: You can open citizens.csv in Microsoft Excel or Google Sheets to view, filter, and analyze the population data.
