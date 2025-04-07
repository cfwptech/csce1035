# csce1035
##Computer Programming I Projects

#Project 2 - Simple Banking System

Simple Banking System: Algorithm and Design Approach

Overview
This Python program simulates a basic banking system where a user can:

- Create an account
- Login
- Deposit funds
- Withdraw funds
- View current balance
- Change password
- Logout

The system handles password encryption, maintains a basic session via global variables, and uses function-based modular design.

1. User Interface Flow
   
The user first creates an account by entering an ID, password, and initial balance.
After account creation, the user sees a menu with numbered options.
The program takes user input and calls corresponding functions based on the selected action.

2. Key Functions and Algorithms
   
a. create_account()
Prompts the user for credentials and initial balance.
Stores all data in a global dictionary called user_account.
Encrypts the password using a Caesar cipher with a shift of 3.

b. encrypt_password(password)
Implements a basic Caesar cipher:
Shifts each character (letters and digits) by 3 places forward.
Leaves symbols unchanged.
Handles uppercase, lowercase, and digits differently using ASCII math.

c. select_choice(user_action)
Acts as the main dispatcher using if-else conditions.
Prompts user to select a menu option (1–6).
Calls appropriate function (e.g., login(), deposit()).

d. login(password_check, user_id)
Verifies user ID and password.
If matched, it allows access to other options by calling select_choice() again.
If incorrect, allows one retry.

e. deposit(amount) and withdraw(amount)
Both modify the current_balance within user_account.
Prompt for the amount and then update the global dictionary.

f. print_balance()
Displays the current balance from user_account.

g. change_password(password)
Asks for current password.
If correct, allows setting a new password.

h. check_id_logout()
Displays a logout message and exits the program.

3. Design Choices
   
Modular Functions: Each operation is in its own function, making it easier to debug and scale.
Global State: user_account holds the session state (not ideal for production, but simple for a learning project).
Input Validation: Limited. Most inputs (like passwords, balance, etc.) are taken without deep validation.
Recursion-like Flow: Many functions call select_choice() again after execution to return to the menu loop.

4. Strengths
   
Simple and beginner-friendly structure.
Demonstrates basic control flow, conditionals, and function use.
Introduces concepts like password encryption and session management.

6. Areas for Improvement
   
Refactor to avoid global variables — consider using classes or passing user_account as a parameter.
Improve password encryption — Caesar cipher is weak and not suitable for real security.
Add input validation and error handling — protect against invalid inputs (like strings in numeric fields).
Fix logic errors — for example, undefined variables like user_action inside some functions.
Implement persistent storage — data is lost once the program ends.


