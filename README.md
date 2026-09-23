# NetworkWalks — Week 3 Project Modules

## 🔐 Password Cracking Labs

This repository contains my Week 3 cybersecurity project work from the NetworkWalks training program.

The two mandatory Week 3 modules demonstrate password recovery techniques using:

- John the Ripper (JTR) and Johnny GUI
- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker

All activities were performed against the authorized training files provided for the lab.

---

## 📂 Project Structure

### W3-PM1 — Password Cracking with JTR

A practical exercise using John the Ripper and Johnny GUI to recover the password of an authorized password-protected PDF.

**Tools:**
- John the Ripper 1.9.0-jumbo-1
- Johnny GUI
- PDF Hash Extractor
- Windows

➡️ [View W3-PM1 Documentation](./W3-PM1-JTR/README.md)

---

### W3-PM2 — Password Cracking with NetworkWalks Tools

A browser-based password recovery exercise using NetworkWalks' Hash Calculator and Password Cracker.

**Tools:**
- NetworkWalks Hash Calculator
- NetworkWalks Password Cracker
- Web Browser
- Windows

➡️ [View W3-PM2 Documentation](./W3-PM2-NetworkWalks-Tools/README.md)

---

## 🎯 Learning Objectives

- Understand how password-protected files can be tested in an authorized security lab.
- Understand the relationship between protected files, hashes, and password recovery.
- Gain practical experience with John the Ripper.
- Understand the use of a graphical interface through Johnny.
- Practice extracting and handling PDF password hashes.
- Understand the basic workflow of browser-based password-cracking tools.
- Learn why weak and predictable passwords present security risks.

---

## 🧪 Lab Workflow

```text
Password-Protected PDF
          │
          ├───────────────┐
          │               │
          ▼               ▼
       W3-PM1          W3-PM2
     JTR / Johnny    NetworkWalks Tools
          │               │
          ▼               ▼
     Hash Extraction   Hash Extraction
          │               │
          ▼               ▼
      Password         Password
       Recovery         Recovery
          │               │
          └───────┬───────┘
                  ▼
           Password Verification
                  │
                  ▼
          Protected PDF Opened
```

---

## 📸 Evidence

Each project folder contains screenshots documenting the corresponding lab steps and results.

---

## 🔒 Authorization & Ethical Use

These techniques were performed only against the authorized training material supplied for the NetworkWalks cybersecurity laboratory.

Password-cracking tools should only be used against files, systems, or accounts for which explicit authorization has been provided.

---

## 📚 Training

**Program:** NetworkWalks Cybersecurity & Ethical Hacking
**Week:** 3
**Modules:** W3-PM1 and W3-PM2

---

## ✅ Status

| Module                                             | Status      |
| --------------------------------------------------- | ----------- |
| W3-PM1 — Password Cracking with JTR                | ✅ Completed |
| W3-PM2 — Password Cracking with NetworkWalks Tools | ✅ Completed |
