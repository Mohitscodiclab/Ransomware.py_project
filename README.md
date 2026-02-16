# 🛡️ Ransomware Simulation Tool for Cybersecurity Education

> ⚠️ **This project is strictly for educational use in a controlled lab environment.
> It is designed to demonstrate how ransomware uses cryptography to deny access to files and to help students understand prevention, detection, and recovery techniques.
> It must NEVER be executed on real user systems or without permission.**

---

## 📌 Project Overview

This project is a **Python-based ransomware behaviour simulator** that demonstrates:

* How files are encrypted using strong cryptographic primitives
* How attackers derive encryption keys from passwords
* How entire directories are targeted
* How a ransom note is dropped after encryption

The goal is **cybersecurity awareness and defensive learning**, not real-world misuse.

---

## 🎯 Learning Objectives

* Understand real-world ransomware workflow
* Learn secure key derivation using **Scrypt**
* Implement **AES-256 encryption**
* Study file system traversal techniques
* Learn the importance of:

  * backups
  * access control
  * endpoint protection
  * incident response

---

## 🧠 Concepts Demonstrated

### 1. Key Derivation – Scrypt

```python
Scrypt(
    salt=salt,
    length=32,
    n=2**14,
    r=8,
    p=1
)
```

Scrypt is used to:

* Convert a password into a **secure 256-bit key**
* Resist brute-force attacks
* Add randomness using a **salt**

---

### 2. AES Encryption (CBC Mode)

The project uses:

* AES-256
* Random IV for each file
* PKCS7 padding

Workflow:

```
File → Read → Pad → Encrypt → Save as .enc → Delete original
```

---

### 3. File System Traversal

```python
os.walk()
```

Used to:

* Recursively locate all files in a directory
* Process them automatically

---

### 4. Ransom Note Generation

After encryption, an HTML file is created to simulate attacker communication.

This demonstrates **social engineering tactics** used in real ransomware attacks.

---

## 🏗️ Project Structure

```
project/
│── ransomware_simulator.py
│── README.md
```

---

## ⚙️ How It Works

1. Detects operating system
2. Selects target directory
3. Reads each file
4. Encrypts file using AES
5. Deletes original file
6. Saves encrypted version
7. Drops ransom note

---

## 💻 Requirements

* Python 3.8+
* cryptography library

Install dependencies:

```bash
pip install cryptography
```

---

## 🚀 Running the Project

### 🔬 SAFE LAB USAGE ONLY

Create a test folder with dummy files:

```bash
mkdir test_lab
```

Run:

```bash
python ransomware_simulator.py
```

---

## 🔐 Decryption (For Educational Extension)

Students can implement:

* Password verification
* Key regeneration using stored salt
* File restoration

This demonstrates **incident recovery techniques**.

---

## 🛡️ Defensive Lessons

This simulation helps understand how to defend against ransomware:

### Prevention

* Regular offline backups
* Least-privilege access
* Email filtering
* Application whitelisting

### Detection

* Monitoring mass file modifications
* Detecting unknown encryption processes
* EDR/XDR solutions

### Response

* Isolate infected machine
* Restore from backups
* Perform forensic analysis

---

## ⚠️ Ethical Use Policy

This project:

✅ Is for education
✅ Is for malware analysis labs
✅ Is for cybersecurity training

❌ Must not be used on real systems
❌ Must not be used for extortion
❌ Must not be deployed without permission

---

## 🎓 Academic Value

This project demonstrates:

* Applied cryptography
* Secure programming
* Operating system interaction
* Cyber attack lifecycle understanding

Perfect for:

* Polytechnic major projects
* Cybersecurity portfolios
* Malware analysis learning

---

## 🔮 Future Enhancements (Defensive Focus)

* File integrity monitor
* Ransomware detection engine
* Backup & auto-restore system
* Real-time encryption alert system
* GUI for awareness training

---

## 👨‍💻 Author

**Mohit Kumar**
🔗 GitHub: [https://github.com/MOHITSCODICLAB](https://github.com/MOHITSCODICLAB)

☕ Support: [https://buymeacoffee.com/MOHITSCODICLAB](https://buymeacoffee.com/MOHITSCODICLAB)

---

## 📜 License

This project is released for **educational and research purposes only**.

---

# ⭐ If you are a cybersecurity student

This project is meant to teach one core truth:

> Understanding how attacks work is the first step to building strong defenses.

