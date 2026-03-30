# 🔧 Cisco IPv4 Connectivity Lab

## 📌 Overview
This lab demonstrates basic configuration, verification, and troubleshooting of IPv4 addressing between two Cisco routers.

---

## 🎯 Lab Objective
To configure IPv4 addresses, verify interface status, and test connectivity between routers.

---

## 🖥️ Topology
R1 ↔ R2 (GigabitEthernet)

- R1: 192.168.10.1/24  
- R2: 192.168.10.2/24  

---

## ⚙️ Configuration

### 🔹 R1 Configuration
enable
configure terminal
hostname R1

interface GigabitEthernet0/0/0
ip address 192.168.10.1 255.255.255.0
no shutdown


---

### 🔹 R2 Configuration
enable
configure terminal
hostname R2

interface GigabitEthernet0/0/0
ip address 192.168.10.2 255.255.255.0
no shutdown


---

## 🔍 Verification

### Show IP Interface Summary
do show ip interface brief


✔ Expected Output:
- Interfaces should be **up/up**
- IP addresses correctly assigned

---

## 🧪 Connectivity Test

From R1:
ping 192.168.10.2


From R2:
ping 192.168.10.1


✔ Successful ping confirms working network

---

## ⚠️ Troubleshooting

Common issues:
- Interface is shutdown → use `no shutdown`
- Wrong IP or subnet mask
- Typo in commands:
show ip interface berif ❌
show ip interface brief ✅


---

## 🧠 Key Learnings
- IPv4 configuration basics  
- Interface activation  
- Verification using show commands  
- Basic troubleshooting skills  

---

## 🚀 Author
Rahat Sahriar Rafi
