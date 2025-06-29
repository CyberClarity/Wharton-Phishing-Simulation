# Wharton Certification Phishing Simulation

## 📚 Overview

This repository documents an **ethical phishing simulation** mimicking a Wharton Academy certification enrollment process. The goal was to demonstrate how social engineering leveraging urgency and trusted brands can trick a target into revealing credentials.

---

## ✅ Objective

- Simulate a targeted phishing attack involving a **fake certification enrollment process**.
- Assess if the target (a consenting friend) would enter credentials on a phishing site posing as Google Sign-In.

---

## 🔎 Attack Workflow

### 1. Data Collection (Pretexting)
- Created a **Google Form** pretending to be a Wharton certification interest form.
- Collected the victim's email under the pretense of enrolling them.

### 2. Crafting the Phishing Email
- Sent a professional-looking email from a spoofed “Wharton Academy” sender.
- Email Subject: **Your Enrollment Process for Wharton Certification**.
- Body informed the victim they needed to “continue enrollment” by clicking a link.

### 3. Setting Up the Phishing Infrastructure
- Used **Gophish** to create a fake **Google Sign-In page** styled identically to the real login page.
- Deployed the phishing page using **Ngrok**, creating a public URL accessible from outside the local network.

### 4. Delivering the Email
- Configured Gophish to send the crafted email directly to the victim’s collected email address.
- Embedded the Ngrok link pointing to the fake login page.

### 5. Victim Interaction
- Victim clicked the “Continue Enrollment” link.
- Victim was redirected to the phishing Google login page.
- Victim entered credentials (email & password).

### 6. Data Capture
- Gophish recorded:
  - The victim’s email address.
  - The password entered.

### 7. Analysis & Findings
- The phishing attempt was successful in capturing valid credentials.
- Demonstrated the effectiveness of urgency (enrollment deadline) and brand trust (Wharton Academy + Google) in phishing attacks.

---

## 📊 Lessons Learned & Recommendations

✅ Even educated targets can fall victim when phishing uses:
- Trusted brands (Wharton, Google).
- Urgency or excitement (certification opportunity).

✅ Organizations and individuals should:
- Carefully inspect sender addresses and links.
- Avoid entering credentials into sites reached through email links without verification.
- Enable **two-factor authentication (2FA)** to reduce credential compromise impact.
- Provide phishing awareness training regularly.

---

## 🖼️ Screenshots

### 📧 Phishing Email
![Phishing Email](https://github.com/CyberClarity/Wharton-Phishing-Simulation/raw/main/mail.jpeg)

### 🌐 Fake Google Login Page (Landing Page)
![Fake Google Login](https://github.com/CyberClarity/Wharton-Phishing-Simulation/raw/main/landing.jpeg)

### 🗂️ Captured Credentials in Gophish
![Captured Credentials](https://github.com/CyberClarity/Wharton-Phishing-Simulation/raw/main/credcap.jpeg)

### 📊 Gophish Campaign Analysis Dashboard
![Gophish Analysis](https://github.com/CyberClarity/Wharton-Phishing-Simulation/raw/main/analysis.jpeg)

---

## 🛠️ Tools Used

- **Gophish**: for creating and managing the phishing campaign.
- **Ngrok**: for tunneling the local phishing site to a public internet URL.
- **Google Forms**: for initial data collection.

---



