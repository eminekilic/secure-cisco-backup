# 🛡️ Secure Network Automation Suite

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)
![Ansible](https://img.shields.io/badge/Ansible-Core-red?logo=ansible&logoColor=white)
![Cisco](https://img.shields.io/badge/Network-Cisco_IOS-black?logo=cisco&logoColor=white)

This repository demonstrates a complete **NetDevOps journey**, evolving from basic Python scripting to scalable Ansible automation. It includes tools for secure configuration backup and infrastructure-as-code (IaC) management.

## 📂 Project Evolution (Structure)

### 1. Python Automation (Scripting)
- **`backup_single.py` (V1):** Connects to a single router defined in `.env`.
  - *Use Case:* Connectivity testing and simple tasks.
- **`backup_multi.py` (V2):** Reads device inventory from `inventory.csv` and processes them in a loop with error handling.
  - *Use Case:* Production backup for multiple devices.

### 2. Ansible Automation (Infrastructure as Code)
- **`ansible/` (V3 - New!):** Contains Playbooks for configuration management.
  - **`router_config.yaml`:** Configures OSPF and Loopback interfaces on multiple routers simultaneously.
  - **`hosts`:** Ansible inventory file.
  - *Use Case:* Mass configuration changes and ensuring state (Idempotency).

## ⚙️ Setup & Usage

### For Python Scripts:
1.  **Install Requirements:**
    ```bash
    pip install -r requirements.txt
    ```
2.  **Configure Credentials:**
    - Create a `.env` file for credentials (IP, Username, Password).
    - For V2, update `inventory.csv` with your device list.
3.  **Run:**
    ```bash
    python backup_multi.py
    ```

### For Ansible Playbooks:
1.  **Navigate to Folder:**
    ```bash
    cd ansible
    ```
2.  **Run Playbook:**
    ```bash
    ansible-playbook -i hosts router_config.yaml
    ```

## 🔮 Future Improvements
- [ ] Integration with Slack/Teams for notification.
- [ ] AI-based Anomaly Detection (Integrating LSTM models).

---
*Developed by **Emine Kılıç** - Computer Engineer & Network Automation Enthusiast*