# 🛡️ Build a SIEM Lab with Splunk — Step-by-Step Guide

---

## 🛠️ Part 1: Prerequisites

| Item | Details |
|:----|:-------|
| Hardware | 8+ GB RAM (16 GB recommended), 2+ CPUs, 100 GB disk space |
| OS | Windows 10/11, macOS, or Ubuntu |
| Virtualization (Optional) | VirtualBox, VMware, Hyper-V |
| Internet Access | Required |

> 💡 **Note:** A separate "attacker" machine (e.g., Kali Linux) is optional but useful.

---

## 🚀 Part 2: Download and Install Splunk

### 1. Create a Splunk Account
- Go to [Splunk Free Download](https://www.splunk.com/en_us/download/splunk-enterprise.html)
- Register and download **Splunk Enterprise** (free trial).

### 2. Install Splunk
- **Windows:** Run the `.msi` installer.
- During installation:
  - Accept License Agreement
  - Choose install directory
  - Set Admin Username & Password
  - Start Splunk as a service (recommended)

---

## 🔧 Part 3: Start and Access Splunk Web

### 1. Start Splunk Service
- **Windows:** Start **Splunkd** service.
<br><img src= "https://i.imgur.com/fy4LfSv.png"><br>
### 2. Access Splunk Web
    - Open your browser.
    - Go to http://localhost:8000
    - Log in with your admin credentials.
  <br><img src= "https://i.imgur.com/Jh16bOq.png"><br>
## Part 4: Set Up Basic Data Sources
Let’s feed it some data!

### 1. Add Local System Logs
In Splunk Web:
- Click Add Data → Monitor
- Choose Local Event Logs (for Windows)
- Add System, Security, and Application logs.
<br><img src= "https://i.imgur.com/p6GJOXK.png"><br>
<br><img src= "https://i.imgur.com/Mrp7vm8.png"><br>
<br><img src= "https://i.imgur.com/uDPD4l7.png"><br>

## Part 5: Install Splunk Universal Forwarder (optional but recommended)
If you want to simulate a real environment where another machine (like a client or server) sends logs:

### 1. Download Splunk Universal Forwarder
      - Download Universal Forwarder
<br><img src= "https://i.imgur.com/CzbXJP5.png"><br>  

### 2. Install on machine
      - Configure it to send data to your Splunk server:
<br><img src= "https://i.imgur.com/CzbXJP5.png"><br>
### 3. Enable Receiving on Splunk Server
        - Go to Settings → Forwarding and Receiving → Configure Receiving
<br><img src= "https://i.imgur.com/3UywL5h.png"><br>
        - Listen on port 9997
<br><img src= "https://i.imgur.com/6cmENgp.png"><br>   
<br><img src= "https://i.imgur.com/VLzwUod.png"><br> 

