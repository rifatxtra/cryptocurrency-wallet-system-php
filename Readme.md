Free Wallet - Cryptocurrency Wallet System (My First PHP Project)
Project Overview
Free Wallet is a comprehensive web-based cryptocurrency wallet management system that allows users to securely store, send, receive, and convert various cryptocurrencies. The system includes both user and admin interfaces with robust functionality for managing digital assets.

Features
User Features
User Authentication: Secure registration and login system with password validation.

Dashboard: Overview of cryptocurrency balances and transaction history.

Asset Management: View and manage multiple cryptocurrencies (BTC, ETH, SOL, BNB).

Transactions: Send and receive cryptocurrencies between users.

Conversion: Convert between different cryptocurrencies.

Deposit/Withdrawal: Deposit funds and withdraw to external wallets.

Profile Management: Update personal information and change passwords.

Transaction History: View all past transactions, deposits, withdrawals, and conversions.

QR Code Generation: For easy receiving of cryptocurrencies.

Admin Features
User Management: View, ban, and unban users.

Transaction Monitoring: Monitor all system transactions.

Deposit/Withdrawal Approval: Review and approve/reject pending transactions.

Address Management: Configure deposit addresses and settings.

System Administration: Comprehensive admin dashboard.

Technology Stack
Frontend: HTML, CSS, JavaScript

Backend: PHP

Database: MySQL

Styling: Custom CSS with glassmorphism design

Security: Password hashing, input validation, session management

QR Code Generation: External API integration

Database Structure
The system uses a MySQL database with the following main tables:

Core Tables
users - Stores user account information

admins - Stores administrator accounts

balance - Tracks user cryptocurrency balances

transactions - Records all peer-to-peer transactions

deposit_history - Tracks deposit requests

withdrawal_history - Tracks withdrawal requests

conversion_history - Records currency conversions

prices - Stores current cryptocurrency prices and fees

deposit_address - Contains wallet addresses for deposits with bonus and fee settings

Installation Guide
Prerequisites
Web server (Apache recommended)

PHP 7.0 or higher with MySQL extension

MySQL database

Modern web browser

Setup Instructions
Clone or extract the project files to your web server directory.

Create a MySQL database and import the provided test.sql schema.

Configure database connection in the admin/config.php file:

PHP

$servername = "localhost";
$username = "your_username";
$password = "your_password";
$database = "your_database";
Set proper file permissions for uploads and temporary files.

Access the application through your web browser.

Default Accounts
Admin Account:

Username: Rifat104

Email: Kop@gmail.com

Password: (set during database import)

User Registration:

Users can register through the signup page with validation for:

Name fields (letters and spaces only)

Username (unique)

Phone number (11 digits starting with 0)

Email (valid format)

Password (minimum 8 characters with uppercase, lowercase, number, and special character)

File Structure
Plaintext

project-root/
├── css/                    # All stylesheets
│   ├── address.css
│   ├── assets.css
│   ├── conversion.css
│   ├── conversionhistory.css
│   ├── deposit.css
│   ├── deposithistory.css
│   ├── login.css
│   ├── overview.css
│   ├── pending.css
│   ├── profile.css
│   ├── receive.css
│   ├── send.css
│   ├── signup.css
│   ├── transaction.css
│   ├── transactions.css
│   ├── users.css
│   ├── withdraw.css
│   └── withdrawalhistory.css
├── images/                 # All project images
│   ├── bitcoin.webp
│   ├── ethereum.webp
│   ├── solana.webp
│   ├── bnb-icon2_2x.webp
│   └── sr_bg.jpg          # Background image
├── admin/                  # Admin panel
│   ├── config.php         # Database configuration
│   ├── index.php          # Admin dashboard redirect
│   ├── login.php          # Admin login
│   ├── address.php        # Address management
│   ├── pending.php        # Pending transaction approval
│   ├── profile.php        # Admin profile
│   ├── transactions.php   # Transaction monitoring
│   └── users.php          # User management
├── dashboard/             # User dashboard
│   ├── index.php          # Dashboard redirect
│   ├── overview.php       # Main dashboard overview
│   ├── assets.php         # Asset management
│   ├── conversion.php     # Currency conversion
│   ├── conversionhistory.php # Conversion history
│   ├── deposit.php        # Deposit functionality
│   ├── deposithistory.php # Deposit history
│   ├── profile.php        # User profile
│   ├── receive.php        # Receive cryptocurrencies
│   ├── send.php           # Send cryptocurrencies
│   ├── transactions.php   # Transaction history
│   ├── withdraw.php       # Withdrawal functionality
│   └── withdrawhistory.php # Withdrawal history
├── login/                 # User login
│   └── index.php
├── signup/                # User registration
│   └── index.php
├── error/                 # Error handling
│   └── error.php
├── index.php              # Landing page
└── test.sql               # Database schema and sample data
Usage Guide
For Users
Registration: Create a new account with validated information.

Login: Access your secure dashboard.

Dashboard: View cryptocurrency balances and recent transactions.

Assets: Manage your cryptocurrency holdings with send/receive options.

Send/Receive: Transfer cryptocurrencies to other users using their User ID.

Convert: Exchange between supported cryptocurrencies.

Deposit: Add funds using provided wallet addresses.

Withdraw: Transfer funds to external wallets.

Profile: Update personal information and change password.

For Administrators
Login: Access admin panel with admin credentials.

Dashboard: Monitor system activity and pending transactions.

User Management: View, ban, or unban users.

Transaction Monitoring: Review all system transactions.

Pending Approvals: Approve or reject deposit and withdrawal requests.

Address Management: Configure cryptocurrency addresses and settings.

System Reports: Generate transaction reports and system analytics.

Security Features
Password Hashing: Uses PHP's password_hash() and password_verify().

Input Validation: Comprehensive validation for all user inputs.

Session Management: Secure session handling with proper logout functionality.

SQL Injection Protection: Prepared statements and input sanitization.

User Authentication: Role-based access control for users and admins.

Ban System: Admin capability to restrict user accounts.

Customization
Styling
Modify CSS files in the css/ directory to change the application's appearance. The design uses a consistent glassmorphism effect with a dark theme.

Cryptocurrencies
To add support for new cryptocurrencies:

Add the currency to the prices table.

Add a column to the balance table.

Update relevant PHP files to handle the new currency.

Add deposit addresses to the deposit_address table.

Update conversion rates and fee structures.

Configuration
Modify admin/config.php for database connection settings and system parameters.

Troubleshooting
Common Issues
Connection Errors: Check database credentials in admin/config.php.

Page Not Loading: Ensure PHP and MySQL are properly installed on the server.

Images Not Displaying: Verify the images directory path is correct.

Functionality Issues: Check if JavaScript is enabled in the browser.

Session Problems: Verify session settings in PHP configuration.

Error Handling
The application includes error handling located in the error/ directory. Error messages are logged and displayed appropriately.

Browser Compatibility
This application works best with modern browsers that support:

HTML5

CSS3

ES6 JavaScript

PHP sessions

Future Enhancements
Two-factor authentication for enhanced security.

Mobile application development.

API integration for real-time price updates.

Enhanced reporting and analytics features.

Multi-language support.

Advanced charting and portfolio analysis.

Email notifications and alerts.

API access for third-party integrations.

Support
For technical support or questions about this application, please refer to the code documentation or contact the development team.

License
This project is proprietary software. All rights reserved.