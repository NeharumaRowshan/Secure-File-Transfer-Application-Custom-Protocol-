# Secure-File-Transfer-Application-Custom-Protocol-
Secure File Transfer Application Using a Custom Protocol

Overview

This project is a Secure File Transfer Application developed in Python that enables encrypted file transmission between a client and a server using a custom communication protocol. The application ensures confidentiality, integrity, and secure key exchange while providing a simple graphical user interface (GUI) for users.

A custom packet-based protocol was designed to handle secure communication, making the application suitable for learning network security concepts and demonstrating secure file transfer techniques.

Features

* Secure file transfer over TCP sockets
* Custom packet-based communication protocol
* End-to-end file encryption using AES-GCM
* Secure ECDH (Elliptic Curve Diffie-Hellman) key exchange
* HKDF-based session key generation
* Graphical User Interface (Tkinter)
* Automatic file encryption and decryption
* Shannon Entropy-based heuristic analysis
* Multi-threaded server for handling multiple client connections
* Cross-platform implementation using Python

Technologies Used

* Python 3
* Socket Programming
* Tkinter
* Cryptography Library
* AES-GCM Encryption
* ECDH Key Exchange
* HKDF Key Derivation
* Multi-threading
* Custom Secure Communication Protocol

How It Works

1. The client connects to the server over a TCP connection.
2. The server and client exchange public keys using ECDH.
3. A shared secret is generated and converted into a secure AES session key using HKDF.
4. The selected file is encrypted with AES-GCM before transmission.
5. The encrypted filename and file data are sent using the custom packet protocol.
6. The server decrypts the received file using the shared session key.
7. Shannon Entropy analysis is performed to identify potentially suspicious files.
8. The decrypted file is securely stored on the server.

Security Features

* Elliptic Curve Diffie-Hellman (ECDH) for secure key exchange
* AES-GCM authenticated encryption
* HKDF-based session key derivation
* Random nonce generation for every encryption operation
* Integrity protection through authenticated encryption
* Custom packet framing with command and payload length fields
* Entropy-based heuristic file analysis

Project Structure

├── client.py          # Console Client
├── gui_client.py      # GUI Client
├── server.py          # Secure Server
├── protocol.py        # Custom Secure Protocol
├── received_files/    # Received files
└── README.md

Educational Purpose

This project demonstrates the practical implementation of secure communication protocols, cryptographic key exchange, authenticated encryption, socket programming, and basic heuristic analysis. It is intended for educational, research, and academic purposes.

Author

Developed as an academic cybersecurity project demonstrating secure client-server communication using a custom protocol.
