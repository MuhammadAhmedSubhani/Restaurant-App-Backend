# Restaurant-App-Backend

# ⚙️ Core Features and Functionality 

1. Login System
The program starts by asking for a username and password.
Access is restricted to admin with password 1234.
Once logged in, it enables full management of the restaurant system.
Includes a logout feature that safely exits the session.

2. Persistent Data Storage (File Handling)
Data for branches, customers, and menu items is stored in plain text files:
branches.txt
customers.txt
menu.txt
On startup, it loads existing data from these files.
On modification, it saves updates back to the files.
This ensures data persists even after the program closes — a lightweight substitute for a database.

3. Fake Data Initialization
If the files are empty, the program automatically populates:
Three branches with preset sales figures.
Three customers with join dates.
Five menu items with prices.
A very practical design choice: ensures your program always has testable data.

4. Branch Management
Add, remove, or list branches.
Each branch stores a name and total sales.
Export feature: creates a CSV sales report (branch_name_sales.csv) for easy access in Excel or Sheets.
Example: exporting Dha Branch creates Dha_Branch_sales.csv.

5. Customer Management
Add, remove, or view customers.
Each record includes the customer name and join date.
Data is saved to customers.txt automatically.
Helps maintain a lightweight customer database.

6. Menu Management
Add, remove, or list dishes.
Each menu item includes a dish name and price.
Data stored in menu.txt, ensuring it persists after exit.
Serves as a simple POS (Point of Sale) backend foundation.

8. Sales Dashboard
Aggregates and displays total data across the system:
Total branches
Total customers
Total menu items
Total sales across all branches
Uses formatted output (iomanip) for a clean, professional terminal display.

# 🧩 Design Strengths

Modular structure: Organized by function groups — file handling, management, login, etc.
File-based persistence: Works even without a database or internet connection.
User-friendly menus: Logical text-based navigation with clear prompts.
CSV export support: Allows integration with spreadsheet tools — a bridge to data analysis.
