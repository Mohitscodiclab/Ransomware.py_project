# 🛡️ RansomwarePy – Cybersecurity Educational Simulator

RansomwarePy is a **Python-based ransomware behaviour simulation tool** created for **cybersecurity education, malware analysis practice, and controlled lab demonstrations**.

It showcases how real-world ransomware:

* derives encryption keys
* encrypts files
* traverses directories
* denies data access

> ⚠️ **This project is strictly for educational and research purposes.
> Do NOT run it on real systems or without explicit permission.**

---

## 🎯 Project Objectives

This project helps students and researchers understand:

* How ransomware encrypts files using strong cryptography
* Why password strength and key derivation matter
* How attackers automate file discovery
* The importance of backup and recovery strategies
* Incident response and defensive security concepts

---

## ✨ Features

* 🔐 **AES-256 File Encryption**
* 🧂 **Scrypt Key Derivation with Salt**
* 📁 **Recursive Directory Processing**
* 🧾 **Ransom Note Simulation (HTML)**
* 🔓 **Recovery / Decryption Module**
* ⚙️ **Cross-Platform Target Detection (Windows/Linux)**
* 🎓 Designed for **Cybersecurity Lab Demonstration**

---

## 🧠 Cryptographic Concepts Used

### Key Derivation – Scrypt

Used to securely convert a password into a 256-bit encryption key.

* Resistant to brute-force attacks
* Uses random salt
* Memory-hard function

### AES-256 (CBC Mode)

Encryption workflow:

```
Original File → Padding → AES Encryption → .enc File → Original Removed
```

Stored format:

```
[salt][IV][ciphertext]
```

This allows the decryption module to regenerate the correct key.

---

## 🏗️ Project Structure

```
RansomwarePy/
│── ransomware.py          # Encryption module
│── decrypt.py             # Recovery / decryption module
│── requirements.txt       # Dependencies
│── README.md              # Project documentation
│── LICENSE
```

---

## 💻 Requirements

* Python 3.x
* cryptography

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ⚙️ Installation

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/Mohitscodiclab/Ransomware.py_project.git
```

### 2️⃣ Navigate into the Project

```bash
cd RansomwarePy
```

### 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

## 🚀 Usage (Lab Environment Only)

### 🔐 Encrypt Files

```bash
python ransomware.py --target /path/to/test_directory --key your_password
```

### 🔓 Decrypt / Recover Files

```bash
python decrypt.py --target /path/to/test_directory --key your_password
```

---

## 🔬 Safe Testing Procedure

1. Create a dummy folder:

```bash
mkdir test_lab
```

2. Add sample files (images, txt, pdf)

3. Run the script on **this folder only**

This prevents accidental data loss.

---

## 🛡️ Defensive Cybersecurity Learning Outcomes

This project demonstrates why the following are critical:

### Prevention

* Regular offline backups
* Least privilege access
* Email attachment filtering
* Application whitelisting

### Detection

* Monitoring mass file modifications
* Identifying unknown encryption processes
* EDR/XDR alerting

### Response

* System isolation
* Restoration from backup
* Forensic investigation

---

## 📚 Academic Value

This project showcases:

* Applied Cryptography
* Secure Programming
* OS File System Interaction
* Malware Behaviour Simulation
* Incident Recovery Techniques

Perfect for:

* Polytechnic Major Project
* Cybersecurity Portfolio
* Viva / Practical Demonstration
* Malware Analysis Learning

---

## 🔮 Future Enhancements (Defensive Focus)

* GUI awareness simulator
* Real-time ransomware detection module
* File integrity monitoring system
* Backup & auto-restore engine
* AES-GCM authenticated encryption upgrade
* Logging & forensic analysis dashboard

---

## ⚖️ Legal & Ethical Disclaimer

This tool is developed **strictly for educational and authorized lab use**.

❌ Do NOT deploy on real systems
❌ Do NOT use for extortion or unauthorized access
❌ Do NOT test without permission

Unauthorized use may violate cybercrime laws.

The author is not responsible for misuse.

---

## 👨‍💻 Author

**Mohit Kumar**
🎓 Polytechnic Student | Aspiring Cybersecurity Specialist

🔗 GitHub: [https://github.com/MOHITSCODICLAB](https://github.com/MOHITSCODICLAB)
☕ Buy Me a Coffee: [https://buymeacoffee.com/MOHITSCODICLAB](https://buymeacoffee.com/MOHITSCODICLAB)

---

## 📖 References

* Wikipedia – Ransomware
* Federal Bureau of Investigation – Ransomware Guidance
* National Cyber Security Centre – Ransomware Overview

---

## 📜 License

This project is licensed under the **MIT License**.
See the `LICENSE` file for details.

---

# ⭐ For Cybersecurity Students

Understanding how ransomware works is the first step toward:

* building detection systems
* designing defenses
* performing malware analysis
* protecting real infrastructure

---

## 🧾 Suggested Resume Description

> Developed a Python-based ransomware behaviour simulator using AES-256 and Scrypt to demonstrate file encryption, key derivation, and incident recovery in a controlled lab environment for cybersecurity education.
