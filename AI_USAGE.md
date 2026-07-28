# AI Improvement Record

## Original Development

The project's design and logic were developed from the project proposal requirements. 
In addition, the foundational schema including menu-driven navigation, variable initialization, nested dictionary structures, and category-specific business logic was drafted manually.
No AI was used during this stage.
## AI Tools Used
JetBrains AI was used in the production of this project primarily by assisting with repetitive lines of code, prediciting future concepts to be used and highlighting incorrect spelling or logic.
## Improvements Requested
- Requests to refine input validation around numerical values (preventing string/negative entries for quantity or income) and file-handling exceptions (IOError, ValueError, KeyError)
- CSV Refactoring: Request to convert the file persistence module from JSON to Python’s native csv library using csv.DictReader and csv.writer, ensuring the flat tabular format correctly mapped to nested dictionaries
- JSON Architecture Generation: Initial request to translate the proposal requirements into a fully functional, modular Python console application utilizing JSON file persistence
## Changes Accepted
- Replaced JSON storage with Python’s built-in csv module (csv.DictReader and csv.writer) and a predefined header array (Category, AvailableUnits, UnitPrice, LeaseRate, ContactNumber)
- Used a Python set() named purchased_types passed between process functions to track unique property classifications accessed during a user session

## Changes Rejected or Revised
- (Rejected Automated Exit Saving) AI originally suggested saving data to the CSV file automatically after every single transaction
- Revised this behavior to align with the proposal’s menu option "Save and Exit". 
  Saving state continuously on every minor action removed user control over canceling session changes.
## What I Learned
- Realized the importance of critically evaluating AI suggestions against strict project constraints such as ensuring data persistence flows strictly follow user menu choices rather than automated background writes
- Gained a practical understanding of how to scope try/except blocks tightly around user inputs and file I/O operations to handle potential crashes gracefully without interrupting the execution loop
