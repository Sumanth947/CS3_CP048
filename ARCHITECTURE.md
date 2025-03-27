# Phonebook Management System - Architecture

## System Architecture

```
                                +-------------------+
                                |                   |
                                |  User Interface   |
                                |  (Menu System)    |
                                |                   |
                                +--------+----------+
                                         |
                                         v
                 +--------------------------------------------+
                 |                                            |
                 |              Core Functions                |
                 |                                            |
                 |  +-------------+       +---------------+   |
                 |  |             |       |               |   |
                 |  | Add Contact |       | Display All   |   |
                 |  |             |       | Contacts      |   |
                 |  +-------------+       +---------------+   |
                 |                                            |
                 |  +-------------+       +---------------+   |
                 |  |             |       |               |   |
                 |  | Search By   |       | Delete        |   |
                 |  | Phone       |       | Contact       |   |
                 |  +-------------+       +---------------+   |
                 |                                            |
                 +--------------------+---------------------+
                                      |
                                      v
                 +--------------------+---------------------+
                 |                                          |
                 |           Data Management                |
                 |                                          |
                 |  +-------------+     +---------------+   |
                 |  |             |     |               |   |
                 |  | In-Memory   |     | File-Based    |   |
                 |  | Storage     |<--->| Persistence   |   |
                 |  | (Array)     |     | (phonebook.txt)|   |
                 |  +-------------+     +---------------+   |
                 |                                          |
                 +------------------------------------------+
```

## Component Description

### 1. User Interface
- **Menu System**: Provides a text-based interface for users to interact with the application
- Handles user input and directs to appropriate functionality

### 2. Core Functions
- **Add Contact**: Adds a new contact to the phonebook
- **Display All Contacts**: Lists all contacts stored in the phonebook
- **Search By Phone**: Finds a contact using their phone number
- **Delete Contact**: Removes a contact from the phonebook

### 3. Data Management
- **In-Memory Storage**: Temporarily stores contacts in an array during program execution
- **File-Based Persistence**: Saves contacts to and loads contacts from a text file (phonebook.txt)

## Data Flow

1. When the application starts, contacts are loaded from the file into memory
2. User interacts with the menu to perform operations
3. Operations are performed on the in-memory data
4. Changes are persisted to the file when contacts are added or deleted
5. When the application exits, all data is saved to the file

## Technical Details

- **Programming Language**: C
- **Data Structure**: Array of Contact structs (maximum 100 contacts)
- **File Format**: CSV-like format with comma-separated values
- **Error Handling**: Basic error handling for file operations and user input

## Limitations

- Maximum of 100 contacts can be stored
- Phone numbers are assumed to be unique
- Limited error handling for file operations