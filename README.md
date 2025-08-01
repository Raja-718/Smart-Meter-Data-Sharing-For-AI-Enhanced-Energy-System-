# 🔐 Smart-Meter Data Sharing for AI-Enhanced Energy System

![Repo Size](https://img.shields.io/github/repo-size/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-?color=blueviolet)
![Stars](https://img.shields.io/github/stars/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-?style=social)
![Forks](https://img.shields.io/github/forks/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-)
![Last Commit](https://img.shields.io/github/last-commit/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-?color=orange)
![License](https://img.shields.io/github/license/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-?color=brightgreen)
![Issues](https://img.shields.io/github/issues/Raja-719/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-?color=lightblue)

---
## 📌 Project Overview

This project presents a two-phase hybrid cryptographic architecture designed to protect smart meter data in intelligent energy systems. It combines **AES-256** for fast encryption, **RSA-OAEP** for secure key exchange, and **SHA-256** for integrity verification. Together, these ensure that billing data remains confidential, verifiable, and resilient against tampering, even when transmitted or stored across distributed infrastructure.

The system further integrates **federated learning** and **blockchain-inspired hash-chain logging**, enabling privacy-preserving model updates and tamper-evident records without centralized data pooling. It supports **token-based searchable encryption**, **secure cloud storage**, and **modular deployment**, making it scalable for smart grid and utility use cases.

---



## 📊 Dataset Details

This project utilizes a **privacy-conscious smart meter billing dataset** that mirrors electricity consumption behavior across various regions and consumer categories. The dataset is structured to support encryption modeling, federated learning, tamper-proof logging, and privacy-preserving search under realistic smart grid conditions.

---

### 📁 Dataset File

| Detail            | Description                           |
|-------------------|---------------------------------------|
| 🗂️ **Filename**   | `Electricity_bill_1k.csv`             |
| 📄 **Format**     | CSV (Comma-Separated Values)          |
| 🔢 **Records**    | 10,000+ (Synthetic + Small Real Sample)|
| 🏗️ **Use Case**   | Encryption, Federated Learning, Search, Tamper Logging |

---

### 🧾 Column Descriptions

| 🏷️ Column Name     | 🔍 Description                                           |
|---------------------|----------------------------------------------------------|
| 👤 Name             | Customer’s full name (anonymized/synthetic)              |
| 🏠 Address          | Customer billing address                                 |
| 🆔 Account ID       | Unique account identifier                                |
| 📞 Phone No.        | Customer's phone number (AES encrypted, if used)         |
| ⚡ Meter No.        | Unique smart meter ID                                     |
| 📅 Date             | Billing date (`YYYY-MM-DD`)                              |
| ⏰ Time             | Time of reading or billing generation                     |
| 🧾 Bill No.         | Unique bill number                                        |
| 📈 Max Demand       | Peak demand during the billing cycle                      |
| 🔁 Previous Unit    | Meter reading at start of billing period                  |
| 🔄 Present Unit     | Meter reading at end of billing period                    |
| 🔢 Billed Unit      | Consumption = Present − Previous                          |
| 📆 Due Date         | Final bill payment due date                               |
| 💰 Total Due        | Total amount to be paid                                   |
| ⚙️ Sanctioned Load  | Approved load capacity for the consumer                   |
| 🧾 Fixed Amount     | Flat billing charges regardless of usage                  |
| 🏷️ Category         | Consumer type (Domestic, Commercial, Industrial, etc.)    |

---

### 📊 Data Characteristics

- 📌 **Includes real + synthetic data** to simulate smart grid scale and diversity  
- 🔐 **Sensitive fields encrypted** using AES and RSA for privacy  
- 📦 **SHA-256 hashing** applied to ensure tamper-evident storage  
- 🕵️‍♂️ **Search enabled** through SHA-256 token-based indexing  
- 🤖 **Used in federated learning** with PyTorch TinyNet + Flower framework  

---

### 🛡️ Privacy & Ethics

- 🔒 No real Personally Identifiable Information (PII) is exposed  
- 🧬 Synthetic data generation ensures ethical, privacy-compliant usage  
- ✅ Aligned with **GDPR principles** and modern data protection standards  



## 🧱 Architecture Diagrams

### 🔹 Detailed System Architecture

![Architecture](Images/Detailed%20System%20Architecture%20Diagram.png)
The system begins with smart meter data generation, which includes sensitive billing details.
This data is secured using hybrid encryption (AES for data, RSA for key, and SHA-256 for integrity).
Encrypted data and hash values are stored in secure cloud storage, with searchable tokens and audit logs.
A blockchain-inspired log ensures tamper detection using previous hash chaining.
Users can search data securely by date, and after decryption and hash verification, the billing info is displayed.


### 🔹 Encryption & Storage Workflow


![Workflow](Images/Data%20Encryption%20and%20Storage%20Workflow.png)


The workflow begins with smart meter data generation, containing sensitive billing and user metadata.
This data is encrypted using AES, ensuring confidentiality, while the AES key is protected using RSA encryption.
A SHA-256 hash is generated from the original data to maintain data integrity and detect tampering.
The encrypted data, AES key, hash, and search token are then stored securely in the cloud.
In parallel, key metadata is logged in a blockchain-inspired audit log for traceability and tamper detection.
This layered encryption strategy ensures secure storage, trusted retrieval, and efficient query support, ideal for smart grid environments.
It balances speed (AES), secure key exchange (RSA), and integrity verification (SHA-256) in a lightweight and scalable manner.


### 🔹 Federated Learning Integration


![System](Images/System%20Architecture%20(Smart%20Meter%20Data%20to%20Global%20Model).png)

Illustrates the end-to-end secure federated learning pipeline for smart meter data analytics.
Raw readings from smart meters are processed at edge devices, where they are encrypted using AES-256-CFB and the key is wrapped using RSA-OAEP.
Encrypted data is then sent to cloud storage for decryption and regional organization, while a tamper-evident hash chain is built in a blockchain-inspired log.
Decrypted region-wise data is locally trained on TinyNet models through Flower clients, preserving data privacy.
The trained weights are securely aggregated via FedAvg on the Flower server to form a global model.
This architecture ensures data confidentiality, tamper detection, and distributed learning without centralized data pooling.
Performance, security, and usability tests confirm the pipeline's scalability, robustness, and real-world deployment feasibility in smart grid environments.

---
## 🛠️ Key Features

- 🔒 **Hybrid Encryption** – Combines **AES**, **RSA-OAEP**, and **SHA-256** for secure, layered protection  
- 🔍 **Privacy-Preserving Search** – Uses tokenized **SHA-256** indexing to enable encrypted queries  
- 🧾 **Blockchain-Inspired Logging** – Lightweight **hash chains** for tamper-evident audit trails  
- ☁️ **Secure Cloud Storage** – Encrypted data, keys, and metadata are stored in a scalable cloud layer  
- 🔓 **Multi-Stage Decryption Workflow** – Supports local AES key decryption with RSA for trusted access  
- ⚠️ **Tamper Detection** – Verifies data integrity with **SHA-256** hash mismatch detection  
- 📈 **Large Dataset Support** – Works with 10,000+ real and synthetic billing records  
- 🔁 **Flexible Query Options** – Search records by exact date or within date ranges  
- 🛡️ **User-Controlled Key Access** – Protects session keys using asymmetric encryption per session  
- 🧠 **Scalable Architecture** – Modular design for integration into real-world grid and utility platforms  
- 🤖 **Federated Learning Ready** – Integrates **TinyNet** + **FedAvg** with secure model aggregation


---
## 🧰 Technologies Used

> A blend of modern cryptography, federated learning, and data engineering tools.

| Technology | Description |
|------------|-------------|
| ![Python](https://img.shields.io/badge/Python-3.10+-blue?logo=python&logoColor=white) | Core language for the complete system pipeline |
| ![Pandas](https://img.shields.io/badge/Pandas-Data%20Handling-black?logo=pandas) | For loading, cleaning, and processing billing data |
| ![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?logo=plotly) | Plotting trends and visualizing smart meter analytics |
| ![Hashlib](https://img.shields.io/badge/Hashlib-SHA256%20Hashing-blueviolet) | Data integrity via SHA-256 hashing |
| ![JSON](https://img.shields.io/badge/JSON-Serialization-lightgrey?logo=json) <br> ![Base64](https://img.shields.io/badge/Base64-Encoding-brightgreen) | Metadata encoding and storage formatting |
| ![Cryptography](https://img.shields.io/badge/Cryptography-AES,%20RSA,%20SHA256-darkgreen?logo=lock) | AES for encryption, RSA for key wrapping, SHA-256 for fingerprinting |
| ![PyTorch](https://img.shields.io/badge/PyTorch-TinyNet-red?logo=pytorch) | Neural networks for federated learning |
| ![Flower](https://img.shields.io/badge/Flower-Federated%20Learning-yellow?logo=flower) | Federated training with secure FedAvg aggregation |
| ![Scikit-learn](https://img.shields.io/badge/Scikit--learn-Feature%20Scaling-fb982e?logo=scikitlearn) | Scales input features using MinMaxScaler |
| ![Concurrency](https://img.shields.io/badge/Concurrent.futures-Parallel%20Tasks-blue) | Speeds up batch encryption/decryption tasks |
| ![Datetime](https://img.shields.io/badge/Datetime%20&%20OS-Logs%20%26%20File%20Handling-lightblue?logo=clockify) | Manages timestamps, file access, and system utilities |


## 📊 Results & Evaluation

This section summarizes the performance and effectiveness of the proposed secure smart meter data system, including encryption validation, tamper-evident logging, federated learning results, and search functionality.

---

### ✅ Encryption & Secure Storage

- 🔐 **AES (CFB mode)** + **RSA (OAEP)** successfully encrypts billing records and session keys.
- 🧩 **SHA-256** hashes ensure integrity; any tampering leads to immediate detection.
- 🧾 **Blockchain-inspired logs** maintain traceable, tamper-evident records for auditability.
- ⚡ Tested on Raspberry Pi–class hardware with average encryption time under **15 ms per record**.

---

### 🔎 Searchable Record Retrieval

- 🔍 Users can retrieve encrypted records using:
  - 📅 **Single Date** query (e.g., `2021-03-15`)
  - 📆 **Date Range** query (e.g., `2021-03-15 to 2021-03-17`)
- 🔓 Retrieved data is **decrypted securely** using RSA and AES keys.
- ✔️ Integrity of the record is verified by comparing hashes from storage and blockchain logs.

---

### 💡 Sample Decrypted Record Output

```json
✅ Decrypted Record:
{
  "meter_id": "12289508",
  "timestamp": "2021-03-15T19:30:45",
  "billed_units": 419,
  "total_due": 3662,
  "region": "Commercial"
}

📜 Blockchain Log Entry:
{
  "entry": {
    "meter_id": "12289508",
    "timestamp": "2021-03-15T19:30:45"
  },
  "hash": "a90c62fb98d095d741250febe8135af4db526bfd972032b283fa211c4ea005c2"
}



