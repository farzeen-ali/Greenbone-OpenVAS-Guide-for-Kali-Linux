# 🌐 Greenbone OpenVAS (GVM) Installation Guide for Kali Linux  

## 📖 Introduction  
Greenbone OpenVAS (also known as GVM - Greenbone Vulnerability Management) is an open-source vulnerability scanner and management tool.  
It helps security professionals and system administrators identify vulnerabilities in their networks and systems.  

---

## ⚖️ Legal Disclaimer  
This tool is intended **only for ethical use** such as penetration testing, research, and system hardening **on systems you own or have explicit permission to test**.  
⚠️ **Unauthorized scanning of networks is illegal and punishable by law.**  

---

## 🚀 Installation & Setup Guide  

### 1️⃣ Update Your System  
```bash
sudo apt update && sudo apt upgrade -y
```
_Update system packages to the latest version._  

---

### 2️⃣ Install Greenbone OpenVAS  
```bash
sudo apt install gvm -y
```
_This will install Greenbone Vulnerability Manager (GVM) and OpenVAS scanner._  

---

### 3️⃣ Setup & Configure GVM  
```bash
sudo gvm-setup
```
_This will automatically set up the database, create an admin user, and configure services._  

---

### 4️⃣ Start All Services  
```bash
sudo gvm-start
```
_Starts the Greenbone services and gives you the web interface URL (usually https://127.0.0.1:9392)._  

---

### 5️⃣ Check GVM Status  
```bash
gvm-check-setup
```
_Verifies that everything is installed and configured correctly._  

---

## 🔄 Feed Updates (To avoid "Feed update in progress" issues)  
Run these commands to manually update feeds if they are stuck:  

```bash
sudo greenbone-feed-sync --type GVMD_DATA
```
_Sync Greenbone Manager data feed._  

```bash
sudo greenbone-feed-sync --type SCAP
```
_Sync SCAP (Security Content Automation Protocol) data feed._  

```bash
sudo greenbone-feed-sync --type CERT
```
_Sync CERT (Computer Emergency Response Team) advisories feed._  

---

## 🎯 Access Web Interface  
After setup, open your browser and go to:  

👉 **https://127.0.0.1:9392**  
_Default user: `admin` (password is generated during setup, check terminal output)._  

---

## 🛠️ Useful Commands  

```bash
sudo gvm-stop
```
_Stop all GVM services._  

```bash
sudo gvm-start
```
_Start all GVM services._  

```bash
sudo gvm-check-setup
```
_Check setup status._  

---

## 👨‍💻 Author  
Made with ❤️ by **The Techzeen**  
