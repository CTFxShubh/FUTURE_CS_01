# FUTURE_CS_01
Implementing Two-Factor Authentication (2FA)

# 2FA Authentication

This application showcases two-factor authentication (2FA) using Time-based One-Time Passwords (TOTP) and QR codes. It enables users to register, log in, and enhance account security through TOTP-based 2FA.

## Features

-> Implements user registration with secure username and password creation.
-> Facilitates user login through password authentication.
-> Enhances security with two-factor authentication (2FA) utilizing Time-based One-Time Password (TOTP).
-> Generates QR codes for seamless 2FA setup and integration.

## Prerequisites

-> Python 3.6 or later
-> Flask framework
-> pyotp library for TOTP
-> qrcode library for QR code generation

## Installation

1. **Clone the repository:**
 
   ```bash
   git clone https://github.com/CTFxShubh/FUTURE_CS_01.git
   cd FUTURE_CS_01
   ```

2. **Install the required packages:**

   ```bash
   pip install Flask pyotp qrcode
   ```

## Usage

1. **Run the Flask application:**

   ```bash
   python app.py
   ```

2. **Open your web browser and navigate to:**

   - `http://127.0.0.1:5000/` - Home page
   - `http://127.0.0.1:5000/register` - User registration
   - `http://127.0.0.1:5000/login` - User login
   - `http://127.0.0.1:5000/2fa` - Two-factor authentication setup

## How It Works

1. **Registration:**

Users create an account with a username and password.
A TOTP secret is generated and securely stored for each user.

2. **Login:**

Users authenticate by providing their username and password.
Upon successful authentication, they are redirected to the two-factor authentication (2FA) setup page.

3. **Two-Factor Authentication:**

Users input the OTP generated by their authenticator app.
The application validates the OTP against the stored TOTP secret.

4. **QR Code Generation:**

A QR code is generated and presented for users to scan with their authenticator app (e.g., Google Authenticator, Microsoft Authenticator).

## Additional Notes

- The application uses an in-memory dictionary (`users`) to store user data. For production use, consider using a database.
- The `secret_key` is used for session management. Change it to a more secure key in a real application.
- Ensure that your application is secure and handle sensitive information appropriately.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

