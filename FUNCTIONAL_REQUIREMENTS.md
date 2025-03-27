# Functional Requirements for Phonebook Management System

## 1. Contact Management
- FR1.1: The system shall allow users to add new contacts with name, phone number, and address.
- FR1.2: The system shall allow users to view all contacts stored in the phonebook.
- FR1.3: The system shall allow users to search for contacts using phone numbers.
- FR1.4: The system shall allow users to delete contacts from the phonebook.

## 2. Data Persistence
- FR2.1: The system shall store contacts in a file named 'phonebook.txt'.
- FR2.2: The system shall load contacts from the file when the program starts.
- FR2.3: The system shall save contacts to the file after adding or deleting contacts.

## 3. User Interface
- FR3.1: The system shall provide a menu-driven interface with the following options:
  - Add Contact
  - Display Contacts
  - Search Contact by Phone
  - Delete Contact
  - Exit
- FR3.2: The system shall display appropriate messages for successful operations and errors.

## 4. Constraints
- FR4.1: The system shall support up to 100 contacts.
- FR4.2: Phone numbers shall be unique identifiers for contacts.