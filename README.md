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

## 💡 Sample Decrypted Record Output


## Demonstration: Search, Decryption, and Audit Logging

![Demonstration](https://github.com/Raja-718/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/raw/main/Images/Demonstrating%20Search%2C%20Decryption%2C%20and%20Audit%20Logging.png)



## 🤖 Federated Learning Performance

Federated training was conducted using region-wise smart meter data frames with **Flower** for orchestration, **TinyNet** for lightweight modeling, and **FedAvg** for secure aggregation. This setup enabled **privacy-preserving learning** across distributed edge devices without centralizing raw data.

---

### 📉 Federated Training Loss over Rounds

![Federated Training Loss](https://github.com/Raja-718/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/raw/main/Images/Federated%20Training%20Loss%20over%20Rounds.png)

🔹 **Description**: Training loss steadily declined over multiple communication rounds, indicating that the global model effectively learned from decentralized, encrypted smart meter data.

---

### 📈 Federated Training Accuracy over Rounds

![Federated Training Accuracy](https://github.com/Raja-718/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/raw/main/Images/Federated%20Training%20Accuracy%20Over%20Rounds.png)

🔹 **Description**: Model accuracy consistently improved across training rounds, reaching **80% by round 3**, validating the effectiveness of secure and collaborative learning without compromising privacy.

---

### 📊 Precision, Recall & F1-Score Across Rounds

![Evaluation Metrics](https://github.com/Raja-718/Smart-Meter-Data-Sharing-For-AI-Enhanced-Energy-System-/raw/main/Images/Federated%20Learning%20Precision%2C%20Recall%2C%20and%20F1-Score%20Across%20Rounds.png)

🔹 **Description**: Evaluation metrics (Precision, Recall, F1-Score) show a positive trend across all rounds, confirming improved generalization and classification quality of the federated model.

---

### 🎯 Summary of Key Metrics

| Metric       | Round 1 | Round 2 | Round 3 |
|--------------|---------|---------|---------|
| 🎯 Precision   | 0.70    | 0.75    | 0.77    |
| 🔁 Recall      | 0.68    | 0.74    | 0.76    |
| 🧮 F1-Score    | 0.69    | 0.745   | 0.765   |
| ✅ Accuracy    | 0.74    | 0.78    | 0.80    |
| 📉 Loss        | 0.0859  | 0.0840  | 0.0835  |

---

### 🔐 Security Validation

- 🔑 **Multi-level Encryption**: Only authorized users can decrypt data using AES + RSA hybrid encryption.
- 📜 **Blockchain-Inspired Logging**: Tamper-evident logs are created using hash chaining.
- ✅ **Hash Integrity Checks**: Every record is validated with SHA-256 before processing or visualization.

---

This federated learning framework demonstrates a secure, decentralized, and ethically grounded approach to smart grid AI — combining **robust cryptographic safeguards** with **scalable, real-time machine learning performance**.





## 🔮 Future Work

While this system already secures and preserves privacy in smart meter data pipelines, several impactful enhancements can be explored in future releases:

---

### 🚀 Scalable Federated Aggregation  
Enhance global model accuracy and robustness by integrating advanced aggregation techniques such as **FedProx**, **SecureBoost**, or **FedNova**, especially in heterogeneous edge environments.

---

### 🧠 Edge Intelligence  
Incorporate lightweight on-device models using **TinyML** or **EdgeTPU** to enable real-time inference and decentralized analytics directly at smart meters.

---

### 🔄 Real-Time Anomaly Detection  
Add streaming-based AI models to detect **fraudulent consumption**, **power surges**, or **meter tampering** on-the-fly, enabling faster alerts and decision-making.

---

### 📊 Visualization Dashboard  
Build a secure, responsive web dashboard for both users and utility providers to **visualize billing trends**, **blockchain logs**, and **federated model performance** in real time.

---

### 🔐 Post-Quantum Cryptography  
Replace classical RSA with **quantum-resistant encryption** methods (e.g., **lattice-based cryptography**) to future-proof the system against quantum computing threats.

---

### 🔍 Semantic Search Capability  
Upgrade token-based search to support **fuzzy**, **semantic**, and **multi-field queries**, enhancing accessibility and usability of encrypted datasets.

---

### 🌐 Cross-Utility Data Sharing  
Implement **secure inter-grid collaboration** using **attribute-based encryption (ABE)** and **blockchain smart contracts** for controlled, verifiable energy data exchange.

---

By addressing these directions, the system can evolve into a comprehensive, scalable, and future-ready platform for smart grid cybersecurity and decentralized AI integration.




## 📄 License

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

This project is licensed under the **MIT License**.

---

MIT License

Copyright (c) 2025 Engineer Raja Babu

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the “Software”), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies
of the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED “AS IS”, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED,
INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A
PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT
HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION
OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE
SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


---

🔗 *To learn more, visit the official MIT license page:* [opensource.org/licenses/MIT](https://opensource.org/licenses/MIT)

---
---

## 🙌 Thanks for Visiting!

Thank you for taking the time to explore this project.  
If you found it helpful or inspiring, please consider dropping a 🌟 — it truly means a lot!

---

### 💬 Let’s Connect & Collaborate

I’m always open to feedback, improvements, or even just a good tech conversation! 😊

- 🐛 **Found a bug?** Feel free to open an issue.  
- 🛠️ **Have an idea?** Pull requests are always welcome.  
- 💬 **Suggestions or thoughts?** Start a discussion!

---

## 📫 Contact Me

📧 **Email:** [engineerrajababu@gmail.com](mailto:engineerrajababu@gmail.com)  
🌐 **GitHub:** [@Raja-718](https://github.com/Raja-718)

---

### 🤝 Let’s Build Secure & Smarter Systems — Together!

> _“I believe in building things that matter — securely, ethically, and openly.”_


