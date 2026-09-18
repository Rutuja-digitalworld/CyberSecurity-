# TASK1:🔐 SIEM – Logs Everywhere

## 📌 What is SIEM?

**SIEM (Security Information and Event Management)** is a core security solution used by a **SOC (Security Operations Center) analyst**.

It helps to:

* Collect logs from different devices
* Centralize logs at one place
* Normalize logs into a common format
* Correlate different logs
* Detect malicious or suspicious activities

---

# 📝 Logs Everywhere

A network contains many devices such as:

* Windows/Linux endpoints
* Servers
* Routers
* Firewalls
* IDS/IPS
* Websites

These devices continuously generate **logs**.

### 🔹 Log Source

A **log source** is any device or system that generates logs.

Logs provide a record or **trail of activities** happening within a network and help analysts detect attacks and troubleshoot problems.

---

# 1️⃣ Host-Centric Log Sources

**Host-centric logs** record activities that happen **within or directly related to a host/device**.

### Examples of Host-Centric Log Sources:

* Windows systems
* Linux systems
* Servers
* Endpoints

### Examples of Host-Centric Activities:

* 👤 User accessing a file
* 🔑 User attempting authentication
* ⚙️ Process execution
* 📝 Creating/editing/deleting registry keys or values
* 💻 PowerShell execution

### ⭐ Easy way to remember:

**Host-Centric = Activity happening INSIDE the computer/host**

---

# 2️⃣ Network-Centric Log Sources

**Network-centric logs** record activities related to **communication between hosts or access to the Internet/network**.

### Examples of Network-Centric Log Sources:

* 🔥 Firewalls
* 🛡️ IDS/IPS
* 🌐 Routers

### Examples of Network-Centric Activities:

* 🔐 SSH connection
* 📁 File accessed through FTP
* 🌐 Web traffic
* 🔑 User accessing company resources through VPN
* 📂 Network file-sharing activity

### ⭐ Easy way to remember:

**Network-Centric = Communication BETWEEN devices/networks**

---

# ⚠️ Problems with Logs

Having many logs creates several challenges for SOC analysts.

## 1. Numerous Log Sources

* A network can have many log sources.
* They can generate **hundreds of events per second**.
* Logs are scattered across different devices.
* Checking every device individually is **time-consuming**.

---

## 2. No Centralization

* Logs remain on the devices where they are generated.
* Analysts may need to connect to each device using **SSH, RDP, etc.**
* Investigating multiple devices separately is inefficient.
* It wastes valuable investigation time.

---

## 3. Limited Context

A single log usually **does not tell the complete story**.

For example:

**File Access → Login → Lateral Movement → Previous Machine Compromised**

Individually, these activities may look normal.

But when the logs are **correlated**, they may reveal a malicious attack.

### ⭐ Key Point:

**Correlation of logs provides better context.**

---

## 4. Limited Analysis

* Thousands of logs can be generated every second.
* Humans cannot manually analyze every single event.
* Important malicious events can easily be missed.

---

## 5. Format Issues

Different devices generate logs in **different formats**.

For example:

* Windows → one format
* Linux → another format
* Firewall → another format
* Router → another format

Analysts would need to understand many different log formats.

---

# 🚨 Why SIEM is Needed

These problems can be solved by using a **SIEM**.

### SIEM helps with:

**Multiple Log Sources**
⬇️
**Centralized Log Collection**
⬇️
**Normalization**
⬇️
**Correlation**
⬇️
**Analysis & Detection**
⬇️
**Identify Security Threats**


---

# ✅ TryHackMe Answers

**1. Is Registry-related activity host-centric or network-centric?**
➡️ **Host-centric**

**2. Is VPN-related activity host-centric or network-centric?**
➡️ **Network-centric**

--------------------------------------

# TASK 2: SIEM – Features

### 🔐 SIEM
<img width="660" height="662" alt="image (59)" src="https://github.com/user-attachments/assets/5064b10b-fafc-4677-911a-ae7af4360703" />

**Security Information and Event Management** is a security solution that collects, normalizes, correlates and analyzes logs from different sources to detect malicious activities.

### 1. Centralized Log Collection

* Collects logs from **endpoints, servers, firewalls, etc.**
* Stores all logs at **one central location**.
* Logs can be collected using **agents or APIs**.
* Eliminates the need to check every machine separately.

### 2. Log Normalization

* Different devices generate logs in different formats.
* **Parsing:** Breaking a log into different fields.
* **Normalization:** Converting logs into a **common consistent format**.

### 3. Log Correlation

* Connects logs from **different sources**.
* Helps identify relationships and attack patterns.
* Example: **Unusual VPN login → File access → PowerShell → Outbound connection**
* Together, these events may indicate **data exfiltration**.

### 4. Real-Time Alerting

* SIEM uses **detection rules** to identify suspicious activity.
* When rule conditions are satisfied → **Alert is generated**.
* Analysts can create **custom detection rules**.

### 5. Dashboards & Reporting

SIEM displays security information through dashboards.

**Examples:**

* Alert Highlights
* Failed Login Attempts
* Events Ingested Count
* Rules Triggered
* Top Domains Visited
* System Notifications
* Health Alerts

### ➕ Other Features

* Threat Intelligence Integration
* Data Retention
* Powerful Searching
<img width="1522" height="846" alt="image (58)" src="https://github.com/user-attachments/assets/018ee54f-8dd2-4a94-bced-1dba1cf0caf3" />

### 📊 Splunk SIEM

* **Splunk** is an example of a **SIEM solution**.
* It provides dashboards for monitoring and analyzing security events.
* A Splunk dashboard can display information such as:

  * Alert Highlights
  * Failed Login Attempts
  * Events Ingested Count
  * Rules Triggered
  * Top Domains Visited


