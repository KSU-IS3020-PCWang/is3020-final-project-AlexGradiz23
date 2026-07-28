# IS 3020 Final Project

## Student and Project Information

- Student name: Alexandra
- GitHub username: AGradiz23
- Project title: Property Registry System
- Application purpose: A registry system that allows instant access to properties available for purchase or leasing while protecting consumer interests.

## How to Run the Application
Python Version: Python 3.8
Required Files: property_registry.py, registry_data.csv

## Major Features
- Registry Lookup: Displays real-time stock levels, purchase prices, monthly lease rates, and consultation details across Residential, Business, and Administrative categories
- Residential Purchasing & Consumer Protection: Allows individual buyers to purchase residential units while enforcing a consumer protection
- Business Procurement & Financial Calculator: Collects business names and expected income metrics
- Administrative Consultation Routing: Captures organizational affiliation and titles for state and municipal representatives
- Data Persistence: Automatically updates inventory stock in real time and saves state changes back to an external CSV file upon program closure
## Python Concepts Used
- Functions:load_data, save_data, display_inventory, process_residential, process_business, process_administrative, and main

- Collections: Uses nested dictionaries for in-memory inventory lookup and a set() data structure to track unique user transactions for consumer protection limit checks

- Conditionals (if/elif/else): Controls main menu routing, evaluates user buy .vs. lease selections, and enforces consumer limits

- Loops (while/for): Uses a while loop for application navigation and a for loop to write rows to the CSV file

- File Persistence: Utilizes Python's csv library to read from and write back to registry_data.csv

- Exception Handling (try/except): Prevents crashes by catching ValueError during non-numeric user inputs
## Data Files
- Category (String): The classification of properties (Residential, Business, or Administrative)
- AvailableUnits (Integer): Current stock count of available units
- UnitPrice (Float): Standard outright purchase price in dollars
- LeaseRate (Float): Base monthly lease cost (applicable to commercial properties)
- ContactNumber (String): Direct line for official consultations (applicable to administrative properties)
## Testing Summary

- Missing File Handling: Deleted registry_data.csv and launched the script. Verified that the application caught the missing file, alerted the user, generated a default registry_data.csv file automatically, and resumed normally.
- Consumer Protection Limit Enforcement: Attempted to make transactions across all 3 property categories in a single run. Verified that after 2 unique categories, the residential procurement module blocked additional unit purchases as intended.
- Data Persistence: Purchased business units and closed the program using menu option 5. Reopened the program and confirmed that remaining unit counts in registry_data.csv reflected the updated inventory.

## AI Use
- Formatting dynamic string templates and currency printing (:,.2f) across console outputs
- Enhancing error resilience with targeted try/except blocks for edge-case file IO and type errors
