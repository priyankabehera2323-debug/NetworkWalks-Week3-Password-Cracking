# W3-PM1 — Password Cracking with JTR

## 📌 Overview

This project demonstrates the process of recovering a password from a password-protected PDF using **John the Ripper (JTR)** with the **Johnny** graphical interface.

The lab involves extracting a crackable hash from an encrypted PDF, loading it into Johnny, running an attack, and verifying the recovered password by opening the file.

This exercise was performed on the authorized training file provided by NetworkWalks.

---

## 🎯 Objectives

- Understand how password-protected files can be tested in an authorized security lab.
- Extract a crackable hash from an encrypted PDF (pdf2john format).
- Load the extracted hash into Johnny, the GUI front-end for John the Ripper.
- Run a password-cracking attack against the hash.
- Verify the recovered password by opening the protected PDF.
- Learn why weak and predictable passwords present security risks.

---

## 🛠️ Tools Used

| Tool                    | Purpose                                             |
| ----------------------- | ---------------------------------------------------- |
| John the Ripper 1.9.0-jumbo-1 | Password-cracking engine                       |
| Johnny GUI               | Graphical front-end for John the Ripper             |
| PDF Hash Extractor (Online HashCrack) | Extract a pdf2john/hashcat-compatible hash from the PDF |
| Windows                  | Lab environment                                     |
| My Locked PDF1.pdf       | Authorized training file                            |

---

## 🔬 Lab Procedure

### Step 1 — Obtain the Training File

Downloaded the authorized encrypted PDF: `My Locked PDF1.pdf`, provided as part of the NetworkWalks Week 3 project module.

### Step 2 — Extract the PDF Hash

Uploaded the protected PDF to the Online HashCrack **PDF Hash Extractor**, which converted the file into a crackable hash (pdf2john / hashcat compatible format) beginning with `$pdf$`.

**Evidence:** `01-jtr-installed.png` / hash extractor output showing the generated `$pdf$` hash.

### Step 3 — Load the Hash into Johnny

Opened Johnny, imported the extracted hash, and confirmed it was recognized under the **PDF** format with the password field showing as uncracked.

**Evidence:** `02-johnny-hash-loaded.png`

### Step 4 — Run the Attack

Started a new attack in Johnny against the loaded hash. John the Ripper worked through its wordlist and successfully recovered the password: **`password1`**.

**Evidence:** `03-johnny-cracked.png` — Johnny showing 100% progress, 1/1 cracked, with the password `password1` displayed against the PDF-format hash.

### Step 5 — Verify and Capture the Flag

Used the recovered password to unlock `My Locked PDF1.pdf`, confirming successful password recovery, and captured the lab's completion flag.

**Evidence:** `04-flag-captured.png` — Flag `nw{networkwalks_flag1_jtr_270521_1}` confirming successful completion of the module.

---

## ✅ Result

| Item              | Value        |
| ------------------ | ------------ |
| Target file        | My Locked PDF1.pdf |
| Hash format         | $pdf$ (pdf2john / hashcat compatible) |
| Cracking tool       | John the Ripper (via Johnny GUI) |
| Recovered password  | `password1` |
| Status              | ✅ Password recovered and PDF unlocked |

---

## 🔒 Authorization & Ethical Use

This technique was performed only against the authorized training material supplied for the NetworkWalks cybersecurity laboratory. Password-cracking tools should only be used against files, systems, or accounts for which explicit authorization has been provided.
