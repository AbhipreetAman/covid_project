**Covid Management System**
Overview
This project is a simple command-line based Hospital Management System designed to manage patient details and their hospital stay information. It includes functionalities for emergency handling, COVID ward management, patient information insertion, updating, searching, displaying, and billing.

**Features**
Emergency Ward Handling: Basic charge information and further procedures for emergency patients.
COVID Ward Management:
New Patient Entry: Insert new patient details.
Update Patient Info: Edit or update existing patient details using the patient ID.
Search Patient: Search for a patient's information.
Display Patients: Display all patient details.
Generate Bill: Calculate the bill for a patient based on the days admitted and delete the patient's entry.

**Data Structures**
Patient Details: The patient information is stored in a doubly circular linked list where each node represents a patient.

**Node Structure:**
struct Patient_Details {
    int Patient_ID;
    int Age;
    char Dept[30];
    char Name[50];
    int Date_Of_Admission[3];
    int Date_Of_Release[3];
    char blood[5];
    char Disease[50];
    char PhNo[15];
    char Gaurdian_name[50];
    char Emergency_contact_no[15];
    char Investigating_Doctor_name[50];
    char available;
    struct Patient_Details* next;
    struct Patient_Details* prev;
};
typedef struct Patient_Details* NODE;

**Functions**
insert(NODE first): Adds a new patient to the list.
ReadData(): Reads patient details from the user.
update(int p_id, NODE first): Updates the details of the patient with the given patient ID.
search(NODE first): Searches for and displays patient information.
Display(NODE first): Displays all patient information.
days_admitted(): Calculates the number of days a patient has been admitted.
bill(NODE first, int days): Generates the bill for a patient based on the days admitted and removes the patient's entry from the list.

**COVID Ward Menu**
New Entry: Prompts the user to input new patient information.
Edit/Update: Updates patient details based on the patient ID.
Search: Searches and displays patient details.
Display: Displays all patient details.
Generate Bill: Generates the bill for a patient based on the number of days admitted and deletes the patient's entry.
Exit: Returns to the main menu.

**Compilation and Execution**
Compile the program using a C compiler:
gcc covid_project.c -o covid_project
Run the executable:
./covid_project
