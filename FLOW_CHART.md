# Phonebook Management System - Flow Chart

```
Start
  |
  v
Initialize Program
  |
  v
Open phonebook.txt file
  |
  v
Load existing contacts
  |
  v
Display Menu
  |
  v
User selects an option
  |
  +----------------+----------------+----------------+----------------+
  |                |                |                |                |
  v                v                v                v                v
Add Contact    Display Contacts  Search Contact   Delete Contact    Exit
  |                |                |                |                |
  v                v                v                v                v
Get contact     List all         Get phone       Get contact      Save changes
details        contacts         number to search   index to delete   |
  |                |                |                |                v
  v                v                v                v             Close file
Add to          Return to        Search for       Remove from        |
phonebook        menu           contact by phone   phonebook         v
  |                                |                |              End
  v                                v                v
Add to file                    Display contact   Update file
  |                                |                |
  v                                v                v
Return to                      Return to        Return to
menu                            menu             menu
```