# 🛡️ Build a SIEM Lab with Splunk — Step-by-Step Guide


## Description
This lab provides a hands-on environment to build and operate a Security Information and Event Management (SIEM) system using Splunk Enterprise. It walks through the complete setup — from installing Splunk, ingesting real system and security logs, to installing security apps, creating alerts, and simulating cyber threats.

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

### 1. Add Local System Logs in Splunk Web:
- Click Add Data → Monitor
- Choose Local Event Logs (for Windows)
- Add System, Security, and Application logs.
<br><img src= "https://i.imgur.com/p6GJOXK.png"><br>
<br><img src= "https://i.imgur.com/Mrp7vm8.png"><br>
<br><img src= "https://i.imgur.com/uDPD4l7.png"><br>

- In the search field search by host="machine_name" or *
<br><img src= "https://i.imgur.com/maAnmOU.png"><br>
- Manually generate some security events:
    - Log failed logins
    - Clear security log
    - Turn Windows Firewall off/on

     
## Part 5: Install Splunk Universal Forwarder (optional but recommended)
If you want to simulate a real environment where another machine (like a client or server) sends logs:

### 1. Download Splunk Universal Forwarder and Install on Machine
  Download Universal Forwarder
<br><img src= "https://i.imgur.com/CzbXJP5.png"><br>  

### 2. Enable Receiving on Splunk Server
  Go to Settings → Forwarding and Receiving → Configure Receiving
<br><img src= "https://i.imgur.com/3UywL5h.png"><br>
        - Listen on port 9997
<br><img src= "https://i.imgur.com/6cmENgp.png"><br>   
<br><img src= "https://i.imgur.com/VLzwUod.png"><br> 

## 📊 Part 6: Install Security Apps on Splunk
### 1. Install Splunk Security Essentials
Apps → Find More Apps → Search "Security Essentials" → Install

## 💥 Part 7: Simulate Security Events
### 1. Generate Events

Manually simulate:

Failed logins

Access forbidden directories

Firewall toggling

## 📚 Part 8: Build Dashboards and Alerts
### 1. Create Dashboards
Save search queries as dashboard panels.
<br><img src= "https://i.imgur.com/yRTiMHb.png"><br>

Deselect _raw and click done

<br><img src= "https://i.imgur.com/gRC2cN8.png"><br>

Navigate to Dashboards- Create New Dashboard- Table

<br><img src= "https://i.imgur.com/YJUo166.png"><br>

<br><img src= "https://i.imgur.com/4DhI8gL.png"><br>

<br><img src= "https://i.imgur.com/bpkFNqh.png"><br>

Paste SPL query
<br><img src= "https://i.imgur.com/2Xe7Htm.png"><br>

Edit Dashboard Visualization to fit specific data (Optional)

<br><img src= "https://i.imgur.com/WJPFMPK.png"><br>

<br><img src= "https://i.imgur.com/W9GCxdu.pngg"><br>

<br><img src= "https://i.imgur.com/scErNQo.png"><br>


