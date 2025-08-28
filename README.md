# Bank Management System

A Java Swing-based ATM simulation application that provides a complete banking interface with user authentication, account management, and transaction processing.

## Features

- **User Authentication**: Secure login with card number and PIN
- **Account Registration**: Multi-step signup process
- **Banking Operations**:
  - Deposit money
  - Cash withdrawal with balance validation
  - Fast cash (₹100 to ₹10,000)
  - Balance inquiry
  - PIN change
  - Mini statement
- **Database Integration**: MySQL for data persistence

## Prerequisites

- Java 8 or higher
- MySQL Server
- JDateChooser library (for date selection)

## Database Setup

1. Create MySQL database:
```sql
CREATE DATABASE bankSystem;
```

2. Create required tables:
```sql
USE bankSystem;

CREATE TABLE login (
    card_number VARCHAR(20),
    pin VARCHAR(10)
);

CREATE TABLE signup (
    formno VARCHAR(20),
    name VARCHAR(50),
    fname VARCHAR(50),
    dob VARCHAR(20),
    gender VARCHAR(10),
    email VARCHAR(50),
    marital VARCHAR(20),
    address VARCHAR(100),
    city VARCHAR(50),
    pincode VARCHAR(10),
    state VARCHAR(50)
);

CREATE TABLE signuptwo (
    formno VARCHAR(20),
    religion VARCHAR(20),
    category VARCHAR(20),
    income VARCHAR(30),
    education VARCHAR(30),
    occupation VARCHAR(30),
    pan VARCHAR(20),
    aadhar VARCHAR(20),
    scitizen VARCHAR(10),
    eaccount VARCHAR(10)
);

CREATE TABLE bank (
    pin VARCHAR(10),
    date VARCHAR(50),
    type VARCHAR(20),
    amount VARCHAR(20)
);
```

3. Update database credentials in `Connn.java`

## Installation

1. Clone the repository
2. Import project into your IDE
3. Add JDateChooser library to classpath
4. Configure MySQL connection in `Connn.java`
5. Run `Login.java` to start the application

## Usage

1. **First Time**: Click "SIGN UP" to create new account
2. **Login**: Enter card number and PIN
3. **Main Menu**: Select desired banking operation
4. **Transactions**: Follow on-screen prompts

## Project Structure

```
src/bank/management/system/
├── Login.java           # Main login interface
├── main_Class.java      # ATM main menu
├── Signup.java          # Registration page 1
├── Signup2.java         # Registration page 2
├── Signup3.java         # Account creation
├── Deposit.java         # Deposit functionality
├── Withdrawl.java       # Withdrawal functionality
├── FastCash.java        # Quick withdrawal
├── BalanceEnquriy.java  # Balance inquiry
├── Pin.java             # PIN change
├── mini.java            # Mini statement
└── Connn.java           # Database connection
```

## Screenshots

### Login Screen
![Login Screen](screenshots/login.png)
*Secure login interface with card number and PIN authentication*

### Main ATM Menu
![Main Menu](screenshots/main_menu.png)
*Professional ATM-style interface with all banking operations*

### Account Registration
![Signup Form](screenshots/signup.png)
*Multi-step registration process for new users*

### Deposit Money
![Deposit](screenshots/deposit.png)
*Easy money deposit with confirmation*

### Balance Inquiry
![Balance](screenshots/balance.png)
*Real-time balance checking*

### Fast Cash Withdrawal
![Fast Cash](screenshots/fast_cash.png)
*Quick withdrawal with predefined amounts*

> **Note**: To add screenshots to your repository:
> 1. Create a `screenshots` folder in your project root
> 2. Take screenshots of each interface
> 3. Save them with the names shown above
> 4. The images will automatically display in the README

## Contributing

1. Fork the repository
2. Create feature branch
3. Commit changes
4. Push to branch
5. Create Pull Request

## License

This project is for educational purposes.
