# Auditing Cloud Activity Using AWS CloudTrail
# Name: THENAMIZHTHAN V
# Register no:212225240175
## 📌 Objective
To audit and monitor cloud activity in AWS using AWS CloudTrail by viewing and analyzing recorded AWS management events. The primary goal is to extract essential audit trail metadata including user identity, event name, event time, AWS service source, target region, read-only status, and operation outcome.

---

## 🛠️ Environment & Prerequisites
* **Cloud Platform:** Amazon Web Services (AWS)
* **AWS Region:** `eu-north-1` (Europe - Stockholm)
* **Services Monitored:** AWS CloudTrail, Amazon S3, Amazon EC2
* **Access Level:** Root / IAM Administrative Rights

---

## 📄 Part A: CloudTrail Setup & Access
1. Navigated to the **AWS Management Console** and accessed **AWS CloudTrail**.
2. Opened the **Event history** dashboard to access log records from the past 90 days of management activity across all supported services.

<img width="1917" height="1078" alt="Screenshot 2026-09-02 202058" src="https://github.com/user-attachments/assets/8de6b99f-58c9-4eda-ba7f-681688b5a455" />

<img width="1917" height="1055" alt="Screenshot 2026-09-02 202118" src="https://github.com/user-attachments/assets/b66e2643-1037-4a30-9093-e14a52655360" />


## 🔬 Part B & C: Detailed Event Analysis

### Event 1: S3 Storage Activity (`CreateBucket`)

<img width="1916" height="1078" alt="Screenshot 2026-09-02 202307" src="https://github.com/user-attachments/assets/07848992-e5a0-444a-9d13-510c05d46aaa" />

---

### Event 2:  AutomatedDefaultVpcCreation

<img width="1917" height="1078" alt="Screenshot 2026-09-02 202340" src="https://github.com/user-attachments/assets/5e1b7b8c-1e3c-4238-8b24-f5f0457e19eb" />

---




## 📋 Part D: Final Security Audit Summary


<img width="900" height="458" alt="Screenshot 2026-09-02 203925" src="https://github.com/user-attachments/assets/a1dbcd2b-9257-48ba-9778-f75dc8a46caa" />

---

## 🔒 Security Audit Findings & Forensic Value
1. **Accountability (Non-repudiation):** CloudTrail logs verify that both critical infrastructure mutations (`CreateBucket` and `AutomatedDefaultVpcCreation`) were performed directly by the `root` account credentials.
2. **Operational Scope:** Isolates the geographic impact (`ap-southeast-2`) and pinpoints exact resource identifiers for targeted incident investigation.
3. **Security Principle:** Identifying frequent `root` user management actions highlights a violation of the Least Privilege Principle; future actions should be performed via specific IAM roles.

---

## ✅ Result
Cloud activity within the AWS environment was audited using **AWS CloudTrail Event History**. Management events were categorized by identity, service source, region, read/write state, and operation status to form an immutable security audit trail.
