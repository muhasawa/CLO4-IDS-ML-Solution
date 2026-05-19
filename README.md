# CLO4-IDS-ML-Solution
Assignment 1 of Information Security course 

# AI-Powered Network Intrusion Detection System (NIDS)

An intelligent, proactive machine learning security tool built to automatically classify enterprise network traffic anomalies and defend against active cyber threats. 

---

## Project Objective
Traditional signature-based perimeters like firewalls often fail to catch zero-day exploits or adaptive attack behaviors. Developed for **SecureNet Corp**, this proof-of-concept project designs and deploys a robust Machine Learning Network Intrusion Detection System (NIDS) utilizing a **Random Forest Classifier**. By analyzing multiple live packet parameters simultaneously, the system shifts our defenses from a reactive, rule-matching posture to proactive, automated threat classification. 

This project fulfills the compliance criteria for **Information Security Assignment 1 (Aligned with CLO 4)**.

---

## Dataset Structure
The architecture leverages the structural schema of the benchmark **NSL-KDD dataset**. It actively models real-world enterprise network vulnerabilities across four primary attack behaviors:
*   **Denial of Service (DoS):** Volumetric attempts to crash servers and exhaust network capacity.
*   **Probing:** Surveillance activities scanning infrastructure for vulnerable entry points.
*   **R2L / U2R:** Brute-force local access breaches and unauthorized administrative privilege escalations.

---

## Dataset Setup & Technical Pipeline
To bypass proxy blockages, local firewall policies, or broken third-party hosting URLs, the implementation pipeline builds a **self-contained, synthetic network telemetry generator** right inside the script. 
* It programmatically produces structurally identical schemas containing features like `src_bytes`, `protocol_type`, and explicit attack vectors.
* The script handles label mapping, converts categorical metadata using `LabelEncoder`, and scales numerical values with `StandardScaler` automatically. **No external dataset downloads are required.**

---

## How to Run the Code

### 1. Prerequisite Installations
Ensure that you have Python installed on your local workstation. Open your **Terminal** (macOS/Linux) or **Command Prompt / PowerShell** (Windows) and execute the following command to download the core data science and machine learning packages:
```bash
pip install pandas numpy scikit-learn matplotlib seaborn
