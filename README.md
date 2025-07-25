# Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-
As smart grids expand with rising electricity demand, securing fine-grained consumption data becomes critical. This Project presents a hybrid cryptographic architecture combining AES-256 for confidentiality, SHA-256 for integrity, and RSA-OAEP for secure key exchange. It enables fast, privacy-preserving search using hash-based queries and ensures tamper-proof logging via a lightweight hash-chain ledger. The system supports encrypted federated learning & analytics and cloud storage with audit-ready metadata. This end-to-end framework addresses key cyber risks—unauthorized access, leakage, and forgery—offering a scalable, standards-compliant solution for secure, intelligent energy networks.

## Detailed System Architecture Diagram
<img src="https://github.com/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/blob/main/Images/Detailed%20System%20Architecture%20Diagram.png"/>
The system begins with smart meter data generation, which includes sensitive billing details.
This data is secured using hybrid encryption (AES for data, RSA for key, and SHA-256 for integrity).
Encrypted data and hash values are stored in secure cloud storage, with searchable tokens and audit logs.
A blockchain-inspired log ensures tamper detection using previous hash chaining.
Users can search data securely by date, and after decryption and hash verification, the billing info is displayed.

## Data Encryption and Storage Workflow 
<img src="https://github.com/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/blob/main/Images/Data%20Encryption%20and%20Storage%20Workflow.png"/>

The workflow begins with smart meter data generation, containing sensitive billing and user metadata.
This data is encrypted using AES, ensuring confidentiality, while the AES key is protected using RSA encryption.
A SHA-256 hash is generated from the original data to maintain data integrity and detect tampering.
The encrypted data, AES key, hash, and search token are then stored securely in the cloud.
In parallel, key metadata is logged in a blockchain-inspired audit log for traceability and tamper detection.
This layered encryption strategy ensures secure storage, trusted retrieval, and efficient query support, ideal for smart grid environments.
It balances speed (AES), secure key exchange (RSA), and integrity verification (SHA-256) in a lightweight and scalable manner.

## System Architecture (Smart Meter Data to Global Model)
<img src="https://github.com/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/blob/main/Images/System%20Architecture%20(Smart%20Meter%20Data%20to%20Global%20Model).png"/>
