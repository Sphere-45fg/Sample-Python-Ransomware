🔐 Python Ransomware Simulation

A simple Python-based ransomware simulation created for educational and ethical cybersecurity practice.

The project demonstrates the basic concept of how file-encrypting ransomware can discover files, generate an encryption key, encrypt file contents, and replace the original contents with encrypted data.

⚠️ WARNING: This project is intentionally designed for cybersecurity education. Do not run it against real or important files, other people's systems, or production environments. Use an isolated test directory or virtual machine containing only dummy files.

📌 Features

🔎 Searches the current directory for files

🔑 Generates a unique Fernet encryption key

🔒 Encrypts discovered files using cryptography.fernet.Fernet

💾 Saves the generated encryption key to thekey.key

🚫 Excludes the ransomware script, encryption key, and decryption script from encryption

📢 Displays a simulated ransom message after encryption

🧠 How It Works

The program follows a basic ransomware workflow:

Start │ ▼ Discover files │ ▼ Exclude protected files │ ▼ Generate encryption key │ ▼ Save encryption key │ ▼ Read file contents │ ▼ Encrypt contents │ ▼ Overwrite original files │ ▼ Display ransom message 

The script uses Python's os module for file discovery and the Fernet implementation from the cryptography package for encryption.

🛠️ Technologies Used

Python 3

cryptography

Fernet symmetric encryption

OS/file-system operations

📂 Project Structure

ransomware-project/ │ ├── malware.py ├── decrypt.py ├── thekey.key └── README.md 

malware.py is the main simulation script.

thekey.key contains the generated encryption key.

decrypt.py is intended for the corresponding decryption process.

⚙️ Installation

Clone the repository:

git clone <YOUR-REPOSITORY-URL> cd ransomware-project 

Install the required Python package:

pip install cryptography 

🧪 Safe Testing

For safe testing, create a dedicated directory containing only disposable test files.

For example:

test-environment/ ├── test1.txt ├── test2.txt ├── notes.txt └── sample.txt 

Do not place personal documents, photographs, credentials, source code, or other important files in the test directory.

A virtual machine can provide an additional layer of isolation.

🔐 Encryption

The script generates a Fernet key and stores it in:

thekey.key 

It then reads the contents of discovered files and encrypts them before writing the encrypted contents back to the files.

💰 Ransom Message

After processing the files, the program displays a simulated ransom demand.

This is included purely to demonstrate the concept of a ransomware attack chain.

No real ransom payment should ever be made.

🎯 Learning Objectives

This project was created to understand:

File-system interaction in Python

File discovery and filtering

Symmetric encryption

Encryption keys

File manipulation

Basic ransomware architecture

How defenders can recognize destructive file-encryption behavior

🛡️ Defensive Security Perspective

Understanding how ransomware works can help cybersecurity professionals identify and defend against it.

Important defensive concepts related to this project include:

Endpoint detection and response (EDR)

File-integrity monitoring

Behavioral detection

Backup strategies

Least privilege

Network segmentation

Incident response

Ransomware detection

Security monitoring and SIEM technologies

⚠️ Disclaimer

This repository is intended strictly for educational and authorized cybersecurity research.

Do not use this software to:

Encrypt someone else's files

Attack computers or networks without authorization

Deploy it on production systems

Destroy or deny access to data

Demand real payment from victims

The author is not responsible for damage caused by misuse of this project.

🚀 Future Improvements

Potential educational improvements include:

Building a safe decryption demonstration

Adding detailed logging

Creating a controlled sandbox environment

Adding file-extension filtering

Creating a ransomware detection component

Monitoring encryption-related file-system activity

Developing a defensive detection rule

👨‍💻 Author

Asiimwe Jordan Reign 

Cybersecurity & Python learning project.

⭐ If you're studying cybersecurity, use this project as a starting point for understanding both how ransomware operates and how defenders can detect it.

