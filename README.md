# 🛡 Linux Hardening Lab

This project documents the steps I took to harden a Linux system against common security risks. The goal is to improve security by applying **best practices in patching, user management, network defense, and monitoring**.  

---

## 🔹 Objectives
- Reduce attack surface on a fresh Linux install  
- Implement security controls following **CIS Benchmarks**  
- Document baseline vs hardened state for learning and reference  

---

## 🔹 Hardening Steps Implemented

### 1. System Updates
- Applied latest patches with `apt update && apt upgrade`  
- Ensures system is not exposed to known vulnerabilities  

### 2. User & Authentication Security
- Disabled root login in SSH  
- Enforced SSH key-based authentication  
- Added fail2ban for brute force protection  

### 3. Network & Firewall
- Configured UFW to allow only necessary traffic (SSH, HTTPS)  
- Default: Deny all inbound, allow all outbound  

### 4. File System & Permissions
- Hardened `/tmp` with `noexec`  
- Restricted sensitive file permissions (`/etc/shadow`)  

### 5. Monitoring & Auditing
- Installed and configured `auditd`  
- Enabled logging for system events and SSH access  

### 6. Security Scans
- Ran **Lynis** audit before and after hardening  
- Reduced warnings from XX → YY (document improvement here)  

---

## 🔹 Results
- Baseline system: vulnerable to weak SSH and default firewall settings  
- Hardened system: restricted access, monitored events, enforced least privilege  

*(Insert before/after screenshots of terminal outputs, configs, and audit scans)*  

---

## 🔹 Tools Used
- **fail2ban** – intrusion prevention  
- **ufw** – firewall management  
- **auditd** – auditing/logging  
- **lynis** – system security auditing  

---

## 🔹 Next Steps
- Automate hardening with Ansible/Terraform  
- Apply CIS Benchmark scripts for further hardening  
- Expand to cloud VM environments (AWS EC2, Azure VM)  
