# Bank-Management
Bank Management System


A brief description of what this project.

Key Features of Your System:

Account Management: Users can create new accounts, log in, and perform transactions securely.

Gift Card Integration: Supports gift card creation, top-up, and redemption.

Reward Points System: Allows users to earn and redeem points based on transactions.

Transaction History: Maintains a log of all user transactions.

Data Persistence: Saves account and transaction data to text files for continuity.

User Interface: Utilizes console-based UI with color-coded messages for better user experience.

Object Oriented Concepts implementation:
1. Core Functionalities
Account Management: Users can create accounts, log in, deposit, withdraw, and view transaction histories.

Gift Card System: Users can generate gift cards, top them up, and redeem purchases using reward points.

Reward Points: Points are earned based on transaction amounts and can be redeemed for discounts.

Transaction Logging: All operations are logged to files, ensuring persistence and traceability.

2. Object-Oriented Design
Base Class: Account
Attributes: Stores account number, username, password, encrypted password, and balance.

Methods:

createAccount(): Prompts user input to create a new account and saves it to a file.

login(): Validates user credentials against stored data.

deposit(float amt): Adds funds to the account.

withdraw(float amt): Subtracts funds, with error handling for insufficient balance.

transactionHistory(): Displays a list of past transactions.

save(): Updates account information in the storage file.

logTransaction(string type, float amt): Records each transaction to a history file.

Derived Class: GiftCard
Additional Attribute: Holds a unique cardID for each gift card.

Methods:

createGiftCard(): Generates a new gift card ID.

topUp(float amount): Adds funds to the gift card.

displayDetails(): Shows account and gift card information.

Further Derived Class: RedeemPoints
Additional Attribute: Manages points earned through transactions.

Methods:

earnPoints(float amount): Calculates and adds points based on the transaction amount.

redeem(float purchaseAmount): Allows users to redeem points for purchases.

redeem(int pts): Redeems a specified number of points for a discount.

showPoints(): Displays the current points balance.

displayDetails(): Shows detailed account information, including points.

Additional Classes
Notifier: Handles user notifications with customizable messages and colors.

AdvancedAccount: Extends Account and Notifier, overriding the deposit method to include notifications.

Operation (Abstract Base Class): Defines a contract for operations like deposit and withdrawal.

DepositOperation: Implements deposit functionality.

WithdrawOperation: Implements withdrawal functionality.

RedeemOperation: Implements redemption of points for purchases.

3. Key Concepts Demonstrated
Polymorphism: Achieved through virtual functions and abstract classes, allowing for dynamic dispatch of methods like perform() in operation classes.

Encapsulation: Sensitive data like passwords are handled securely, and account details are managed through getter and setter methods.

Abstraction: Complex operations are abstracted into classes and methods, providing a clear interface for users.

Inheritance: Allows for code reuse and extension, as seen in the GiftCard and RedeemPoints classes inheriting from Account.
en.wikipedia.org

4. User Interface
Splash Screen: Displays a welcome message with a loading animation.

Main Menu: Offers options to create an account, log in, or exit the system.

User Menu: Provides authenticated users with options to perform various account operations.

Input Validation: Ensures that user inputs are of the correct type and handles errors gracefully.

5. File Handling
Account Storage: Account information is stored in accounts.txt.

Transaction History: Each account has a corresponding history file named <accNumber>_history.txt.

Data Persistence: Changes to account balances and transaction logs are saved back to the respective files.

6. Enhancements and Considerations
Security: Implementing stronger encryption for passwords and sensitive data.

Error Handling: Adding more robust exception handling and input validation.

User Experience: Improving the user interface with better formatting and clearer prompts.

Scalability: Considering the use of databases for handling larger volumes of data.
