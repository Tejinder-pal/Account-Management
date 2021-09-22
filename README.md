***ACCOUNT MANAGEMENT SYSTEM***

1	Business Requirements & Rules
      •	System will have 2 roles Bank Manager & Account Holder
      •	Bank Manager will check if there are any accounts for PAN Card number of the applicant. If NO account exists for PAN CARD number then - Bank Manager will enter Applicant         Name, Date of Birth, PAN Card No, Aadhar Number, Postal Address, Date Of Birth, Email Address at the time of opening account. Scanned copies of Pan Card & Aadhar Card           (Any Image file) will be uploaded at the time of submitting new application.
      •	Upon submission of account opening form new account number (10 digits) will be generated.
      •	If there already exists an account for same PAN CARD number in the bank no new Customer ID (6 digits) will be generated else new Customer ID will be generated.
      •	New Account will be linked to existing (or newly generated) Customer ID. Customer ID can have multiple linked accounts. Customer ID will be the login id for the account        holder.
      •	If Customer ID is newly generated a mail will be sent to the account holder giving the login id (Customer ID) and temporary system generated password.
      •	If account holder logs into the system for the first time with temporary password he / she will be forced to change the password and has to login again with new                password.
      •	Once Account holder successfully log in account holder should be shown all linked accounts with current balances. On Clicking of any account user should shown last 5             transactions of that account.
      •	There should be a provision to show transactions from a user specified date range. User (Account Holder) can export the transactions in CSV format
 



•	Account Operations
      o	Supported types of transactions - Cash Withdrawal, Cash Deposit, Account Transfer
      o	There is no limit to number of deposits per day in the account.
      o	Cash withdrawal will be limited to maximum of INR 10000/ day.
      o	Account Holder can select option of deposit or withdrawal (ATM simulation), Amount for deposit & Withdrawal
      o	For withdrawal - in case of insufficient balance or per day withdrawal limit exceeding user should be shown appropriate error message
      o	If deposit / withdrawal is successful email will be sent to the user (Account Holder) that deposit / withdrawal transaction has occurred in the account (mention masked           Account number) and amount.
      o	There should be a screen where account holder can transfer from any his
      / her own account to another account (of the user of someone else). User should sect from account number from linked accounts, enter the target account number and amount.          Transaction should be rejected for insufficient funds. On success both sender and receiver will get mails of transfer and credit respectively to their accounts.
      o	Any cash deposit / withdrawal or transfer transaction will have a unique transaction reference number


2	System Roles (Actors)
    •	Bank Manager
    •	Account Holder
 



3	Suggested Classes
      •	Role – Role ID , Name
      •	Bank Customers (Customer ID, PAN Card, Aadhar Number, Name, Postal Address, Email, PAN Card, Date of Birth)
      •	Bank Account (Account Number, Customer ID, Current Balance)
      •	Account Transaction (Transaction ID, Transaction reference number, Date Time, Type (Debit/Credit), SubType (Cash/Transfer), Current Balance
      •	Users (User Id, Password, Role)

4	Use cases (Screens)
      •	Role Bank Manager (Assume bank manager user id and password is initially populated via backend SQL)
      o	Query if there is account for given pan card number
      o	Create New Account
      •	Role User
      o	View Accounts – Linked to customer ID
      o	View Mini Statement (Last 5 transactions) – for selected account
      o	View Date Specific Account Statement - Export
      o	Cash Withdrawal & Deposit
      o	Account Transfer
      •	Mail Provision
