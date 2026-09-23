# W3-PM2 — Password Cracking with NetworkWalks Tools

## 📌 Overview

This project demonstrates the basic process of recovering a password from a password-protected PDF using NetworkWalks' browser-based security tools.

The lab involves extracting the password hash from an encrypted PDF using the **NetworkWalks Hash Calculator** and then using the **NetworkWalks Password Cracker** to recover the password.

This exercise was performed on the authorized training file provided by NetworkWalks.

---

## 🎯 Objectives

- Understand the basic concept of password cracking.
- Extract password-related hash data from a protected PDF.
- Use the NetworkWalks Hash Calculator to generate a PDF hash.
- Use the NetworkWalks Password Cracker to attempt password recovery.
- Verify the recovered password by opening the protected PDF.
- Understand why weak passwords are vulnerable to cracking attempts.

---

## 🛠️ Tools Used

| Tool                          | Purpose                                          |
| ----------------------------- | ------------------------------------------------ |
| NetworkWalks Hash Calculator  | Extract the password hash from the protected PDF |
| NetworkWalks Password Cracker | Attempt to recover the PDF password              |
| Web Browser                   | Access the online tools                          |
| Windows                       | Lab environment                                  |
| My Locked PDF1.pdf            | Authorized training file                         |

---

## 🔬 Lab Procedure

### Step 1 — Obtain the Training File

Downloaded the authorized encrypted PDF:

`My Locked PDF1.pdf`

The file was provided as part of the NetworkWalks Week 3 project module.

---

### Step 2 — Generate the PDF Hash

Opened the NetworkWalks Hash Calculator and uploaded the protected PDF.

The tool identified the PDF as encrypted and generated a crackable hash (pdf2john / hashcat compatible format) beginning with:

```text
$pdf$
```

The complete generated hash — including revision, version, and key length details (Revision: R4, Version: V4, Key length: 128 bit) — was copied for the next stage.

**Evidence:** `01-hash-calculator.png` — Hash Calculator output showing the generated PDF hash.

---

### Step 3 — Submit the Hash to the Password Cracker

Opened the NetworkWalks Password Cracker and entered the complete PDF hash generated in the previous step.

The password-cracking process was then started, running a dictionary attack that tried each word from a wordlist against the hash — the same underlying approach used by John the Ripper.

**Evidence:** `02-password-cracker.png` — Password Cracker progress view showing candidate words being tried against the hash.

---

### Step 4 — Recover and Verify the Password

The dictionary attack matched the hash against the candidate `password1`, and the tool reported the password as cracked successfully.

Used the recovered password to unlock `My Locked PDF1.pdf`, confirming the password worked and the file opened successfully.

**Evidence:** `03-password-recovered.png` — Password Cracker showing "PASSWORD CRACKED SUCCESSFULLY" with the recovered password `password1`.

---

## ✅ Result

| Item              | Value        |
| ------------------ | ------------ |
| Target file        | My Locked PDF1.pdf |
| Hash format         | $pdf$ (pdf2john / hashcat compatible) |
| Cracking method     | Dictionary attack (NetworkWalks Password Cracker) |
| Recovered password  | `password1` |
| Status              | ✅ Password recovered and PDF unlocked |

---

## 🔒 Authorization & Ethical Use

This technique was performed only against the authorized training material supplied for the NetworkWalks cybersecurity laboratory. Password-cracking tools should only be used against files, systems, or accounts for which explicit authorization has been provided.
