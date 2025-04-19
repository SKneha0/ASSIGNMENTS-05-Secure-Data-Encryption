Secure Data Encryption System with Streamlit 🔒
Project Overview
The Secure Data Encryption System is a Python-based application that allows users to securely store and retrieve data using encryption techniques. The system uses Streamlit for the front-end UI and implements symmetric encryption (Fernet) to ensure data privacy. Users can store and retrieve encrypted data using a unique passkey, and the system includes mechanisms to protect against failed login attempts.

Features
Data Storage: Store data securely with encryption and a unique passkey.

Decryption: Retrieve the encrypted data by providing the correct passkey.

Failed Attempts Handling: After three failed attempts, users are redirected to the login page for reauthorization.

User Interface: Simple and user-friendly interface built with Streamlit.

Technologies Used
Python: The primary programming language.

Streamlit: For the user interface (UI).

Cryptography (Fernet): For symmetric encryption (data encryption and decryption).

hashlib: For hashing the passkey (SHA-256).

UUID: For generating unique data IDs.

Base64: For encoding the encryption key.

Installation
1. Clone the Repository
bash
Copy
Edit
git clone <your-repository-url>
2. Install Dependencies
Ensure that you have Python installed (preferably version 3.x).

Use the following command to install the required packages:

bash
Copy
Edit
pip install -r requirements.txt
Alternatively, install the individual packages:

bash
Copy
Edit
pip install streamlit cryptography
3. Run the Application
After installation, run the application using Streamlit:

bash
Copy
Edit
streamlit run secure_data_app.py
This will start the Streamlit server and open the application in your web browser.

How to Use
Home Page:

Navigate to Home and choose to either Store New Data or Retrieve Data.

Store Data:

Enter your data and a passkey.

If the passkey is correct, the data will be encrypted and stored securely.

The Data ID will be shown, which is necessary to retrieve the data later.

Retrieve Data:

Provide the Data ID and the passkey.

If the passkey is correct, the data will be decrypted and displayed.

If the wrong passkey is entered three times, you will be redirected to the Login Page.

Login Page:

After too many failed attempts, reauthorization is required by entering the correct master password.

Security Features
Fernet Encryption: The system uses Fernet symmetric encryption for secure data storage.

Passkey Hashing: Passkeys are hashed using SHA-256 to ensure they are not stored in plain text.

Failed Attempt Lockout: After three failed attempts, the user is locked out for a brief period before being allowed to try again.

Challenges Overcome
Control Flow Mastery: Implemented loops, conditions, and validation checks to handle failed attempts and data retrieval.

Multiple Data Types: Handled strings, dictionaries, and encryption handling to ensure secure data management.

Encryption Basics: Used Fernet encryption for symmetric encryption and decryption.

Real-World UI: Integrated a user interface with Streamlit for data interaction.

Error Handling: Implemented error handling for incorrect inputs, failed attempts, and redirection.

Further Improvements
Data Persistence: Currently, data is stored in memory. It can be persisted to a file (e.g., JSON) for future use.

Advanced Security: Switch to PBKDF2 hashing for additional security.

Time-based Lockout: Implement a lockout timer for failed login attempts.

Multi-User Support: Allow different users to store and retrieve their data securely.

Contributing
Feel free to contribute to this project! If you find any bugs or have ideas for improvements, please create an issue or submit a pull request.

License
This project is licensed under the MIT License - see the LICENSE file for details.

Acknowledgments
Streamlit: For providing a simple and powerful tool for creating interactive web apps.

Cryptography: For making encryption easy to implement.

Python: For being a versatile and powerful programming language.