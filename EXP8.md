# Ex.No: 8  Test cases for Banking Application

### DATE:  05-02-2025                                                                          
### REGISTER NUMBER : 212221045003
### AIM: 
For Banking Applicationsystem study its system specifications and generate test cases.
### The characteristics of a Banking application are as follows: 

### Requirement Gathering: 
Test Case ID: RG-01
Description: Validate that all user requirements for opening a bank account are documented.
Expected Result: All requirements are complete and approved by stakeholders.
### Requirement Review: 
Test Case ID: RR-01
Description: Review the documented requirements for consistency and clarity.
Expected Result: All requirements are clear and unambiguous.

### Business Scenario Preparations: 
Test Case ID: BS-01
Description: Prepare business scenarios for different types of accounts (savings, checking, etc.).
Expected Result: Scenarios accurately reflect real-world banking situations.


### Test Case Preparation: 
Test Case ID: TC-01
Description: Create test cases for opening a savings account.
Expected Result: All necessary test cases are prepared.

### Test Case Review: 
Test Case ID: TCR-01
Description: Review test cases for accuracy and completeness.
Expected Result: Test cases are approved and ready for execution.

### Test Case Execution: 
Test Cases for Opening a Bank Account
Test Case ID: TC-02

Description: Verify successful opening of a savings account with valid input parameters.
Input Parameters:
Account Type: Savings
Customer Name: John Doe
Initial Deposit: $500
Email: john@example.com
Phone Number: 1234567890
Expected Result: Account is created successfully, and confirmation is received.
Test Case ID: TC-05

Description: Validate that the system allows the selection of different account types.
Input Parameters:
Account Type: Checking
Expected Result: Account of type Checking is successfully created.
### Database Testing: 
Test Case ID: DB-01
Description: Verify that the account details are stored correctly in the database after successful account creation.
Expected Result: Database reflects the correct details (Account Type, Customer Name, etc.).

### Security Testing: 
 Test Case ID: ST-01
Description: Test for SQL injection vulnerabilities during account creation.

### Input parameters checking: 
 Input Parameters:
Customer Name: "John'; DROP TABLE Accounts; --
Expected Result: System should not allow execution of SQL commands; error is displayed.
Test Case ID: IPC-01
Description: Validate system response to empty required fields during account creation.
Expected Result: Error messages are displayed for all required empty fields.

### Test cases for opening bank account:
Test Case ID: IPC-01
Description: Validate system response to empty required fields during account creation.
Expected Result: Error messages are displayed for all required empty fields.

### Type of account: 
Test Case ID: TA-01
Description: Verify that the system allows users to select only valid account types.
Input Parameters:
Account Type: InvalidType
Expected Result: Error message "Invalid account type" is displayed.

### Test cases: 
Test Case 7: Invalid Account Type Selection
Test Case ID: TC-007
Description: Verify that the system allows users to select only valid account types.
Preconditions: User is on the account creation page.
Input Parameters:
Account Type: InvalidType
Customer Name: John Doe
Initial Deposit: $500
Email: john@example.com
Phone Number: 1234567890
Expected Result: Error message "Invalid account type" is displayed.



### Result:
Thus, the Test cases for Banking Application is implemented and output is verified successfully. 
