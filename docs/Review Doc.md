## This project is an Expense Tracker written in Python that allows users to input their expenses, save them to a file, and summarize their spending. Here's a breakdown of its functionality:

# Main Function:
  - Prints a message indicating the tracker is running.
  - Sets the path to the expense file and a budget limit.
  - Gets user input for an expense.
  - Saves the expense to a file.
  - Summarizes all expenses from the file and compares them to the budget.

# Getting User Expense:
  - Prompts the user to enter the name and amount of the expense.
  - Displays a list of categories and asks the user to select one.
  - Creates an Expense object with the provided details.

# Saving Expense to File:
  - Appends the expense details (name, amount, category) to the specified file.

# Summarizing Expenses:
  - Reads all expenses from the file.
  - Categorizes and sums the expenses.
  - Displays the total amount spent per category, total spending, remaining budget, and the daily budget for the rest of the month.

# Green Text Function:
  - Returns text formatted in green color for terminal output.
  - Overall, this project provides a basic yet functional expense tracking system, allowing users to manage and review their finances on a monthly basis.


# Here’s how it functions:

# Starting the Application:
The user runs the script, and the application prints:
Running Expense Tracker!

# Getting User Expense:
The application prompts the user to enter the name of the expense:

Enter expense name: [user inputs "Groceries"]
Then, it asks for the expense amount:

Enter expense amount: [user inputs "150.00"]
Next, it displays the categories and asks the user to select one:

Select a category: 
  1. Food
  2. Bills
  3. Work
  4. Debt
  5. Fun
  6. Misc
Enter a category number [1 - 6]: [user inputs "1"]
The application then creates an Expense object with the details provided.
Saving Expense to File:

The application appends the expense to the file and confirms:
Saving User Expense: Expense(name='Groceries', amount=150.0, category='Food') to expenses.csv

# Summarizing Expenses:
The application reads all expenses from the file and categorizes them.

It prints the expenses by category:

Expenses By Category:
  Food: $150.00
It prints the total amount spent:
Total Spent: $150.00
It calculates and prints the remaining budget:
Budget Remaining: $1850.00
Finally, it calculates and prints the daily budget for the rest of the month:
Budget Per Day: $61.67


# During the development of the expense tracker, several issues arose. Here’s a detailed account of the challenges faced and how they were addressed:

# 1. File Handling
Issue:
Initially, managing the expense data in a file posed some challenges. For instance, appending data to the file needed to be done carefully to avoid overwriting existing data.

Solution:
The solution was to open the file in append mode ("a") when writing new expenses. This ensured that new expenses were added to the end of the file without affecting the existing data.

# 2. Data Validation
Issue:
Getting user input for expense amount and category required validation to ensure that the entered data was appropriate (e.g., the amount should be a number, and the category should be within the given options).

Solution:
To address this, input validation was implemented:

For the expense amount, the input was converted to a float and wrapped in a try-except block to handle invalid entries.
For the category selection, a while loop ensured that the user could only select from the provided options.

# 3. Reading and Summarizing Data
Issue:
Reading the expense data from the file and summarizing it correctly was crucial. Incorrect parsing of the file data could lead to inaccurate summaries and budget calculations.

Solution:
When reading the file, the data was split and parsed correctly into the respective expense attributes. Additionally, a dictionary was used to aggregate expenses by category, ensuring that the data was processed accurately.

# 4. User Interface
Issue:
Providing a user-friendly interface in the terminal was challenging. Ensuring that prompts and outputs were clear and intuitive required careful consideration.

Solution:
Using clear and consistent print statements helped create a more user-friendly interface. Additionally, using emojis added a visual element to differentiate various parts of the process, making it more engaging for users.

## Expense Tracker, version 2:

# Milestone 1: Enhanced User Input Validation
Description: Improve the user input validation to make the expense tracker more robust. This includes handling edge cases, such as negative expense amounts or invalid category inputs, and providing clear error messages to guide the user.

Tasks:

Implement validation for negative or zero expense amounts.
Ensure category selection is within the valid range.
Add user-friendly error messages for invalid inputs.
Test with various invalid inputs to ensure robustness.

# Milestone 2: Expense Editing and Deletion
Description: Add functionality to edit and delete existing expenses. This will allow users to correct mistakes and manage their expenses more effectively.

Tasks:

Implement a function to list all expenses with an index.
Allow users to select an expense to edit or delete based on the index.
Implement the logic for editing an expense (modifying name, amount, or category).
Implement the logic for deleting an expense.
Update file handling to reflect these changes.

# Milestone 3: Category Management
Description: Introduce the ability for users to manage categories. Users should be able to add, remove, and rename expense categories to better suit their needs.

Tasks:

Implement functions to add new categories.
Implement functions to remove existing categories.
Implement functions to rename categories.
Ensure that category changes are reflected in existing expenses.
Update the user interface to support category management.
Milestone 4: Graphical Summary of Expenses
Description: Enhance the expense summary with graphical representations, such as pie charts or bar graphs, to provide a visual breakdown of expenses by category.

Tasks:

Research and select a Python library for creating graphs (e.g., Matplotlib, Seaborn).
Implement functions to generate pie charts or bar graphs of expenses by category.
Integrate the graphical summary into the existing summarize_expenses function.
Test the graphical output with various datasets to ensure accuracy.

# Milestone 5: Monthly Expense Reports
Description: Add functionality to generate monthly expense reports. This will allow users to view and save their expense summaries for each month.

Tasks:

Implement logic to filter expenses by month.
Create a function to generate a detailed monthly report, including a graphical summary.
Allow users to save the monthly report as a file (e.g., PDF or CSV).
Test the monthly report generation with data from multiple months.

# Milestone 6: User Interface Improvements
Description: Refine the user interface to enhance usability and aesthetics. This includes better prompts, clearer instructions, and an overall more polished look.

Tasks:

Review and improve all print statements for clarity and consistency.
Add color coding or formatting to differentiate various sections (e.g., error messages, summaries).
Implement a main menu for easier navigation between features (e.g., adding expenses, viewing summaries, managing categories).
Collect feedback from users and iterate on the design.

# Milestone 7: Backup and Restore Functionality
Description: Add backup and restore functionality to ensure that users can safeguard their data and restore it in case of loss or corruption.

Tasks:

Implement a function to create a backup of the expense file.
Implement a function to restore expenses from a backup file.
Provide options for automatic and manual backups.
Test the backup and restore functionality to ensure data integrity.
These milestones provide a structured path for enhancing the Expense Tracker, ensuring that each feature builds on the previous ones and the project progresses smoothly towards a more robust and user-friendly version 2.

## Self Reflection
# Satisfaction with Progress
I'm satisfied with the progress made so far. The core functionality of the expense tracker is working well, allowing users to input expenses, save them to a file, and summarize them effectively. The foundational aspects are solid, and the project is ready for the next phase of enhancements and refinements.

Feasibility of Finishing Within the Next Weeks
Yes, I believe the project can be finished within the next few weeks. The milestones outlined provide a clear roadmap, and by focusing on one milestone at a time, the enhancements can be systematically implemented. Each milestone is broken down into manageable tasks, making the overall goal achievable within the given timeframe.

# Expectations vs. Reality
# Easier Than Expected:

Basic File Handling: Managing the reading and writing of expenses to a file turned out to be straightforward once the correct file modes and parsing methods were applied.
User Interface Design: Adding emojis and structured print statements to create a user-friendly interface was easier than anticipated. It added a nice touch to the application with minimal effort.

# More Difficult Than Expected:

Input Validation: Ensuring robust validation for user inputs required more attention than initially expected. Handling various edge cases and providing meaningful error messages added complexity.
Summarizing Expenses: Aggregating expenses by category and ensuring the accuracy of the summaries involved meticulous parsing and data manipulation, which was more intricate than initially thought.
Light Bulb Moments
Importance of Validation: During the development process, it became evident that robust validation is crucial for a smooth user experience. This realization came from encountering various edge cases where invalid inputs could disrupt the application's flow.
User-Centric Design: Adding visual elements like emojis and formatting made the application more engaging and easier to use. This was an unexpected yet valuable insight into how small design choices can significantly impact user experience.
Graphical Representation: While planning for future milestones, the idea of adding graphical summaries (e.g., pie charts, bar graphs) highlighted the potential for visual data representation to enhance the application's utility. This realization came while thinking about how to make the expense summaries more insightful for users.
