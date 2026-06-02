# ⚙️ Splunk Deployment Steps

## 📌 Overview
This document explains the step-by-step process of setting up a basic Splunk architecture including Forwarder, Indexer, and Search Head.

---

## 🛠️ Step 1: Install Splunk Enterprise (Indexer & Search Head)

1. Download Splunk Enterprise from official website
2. Install on server / local machine
3. Start Splunk service

Command:
./splunk start

---

## 🛠️ Step 2: Configure Indexer

1. Login to Splunk Web (http://localhost:8000)
2. Create Index:
   Settings → Indexes → New Index
3. Configure data storage for logs

---

## 🛠️ Step 3: Install Universal Forwarder (Log Source)

1. Download Splunk Universal Forwarder
2. Install on source system
3. Configure inputs.conf

Example:
[monitor:///var/log/syslog]
index=main

---

## 🛠️ Step 4: Connect Forwarder to Indexer

Command:
./splunk add forward-server <indexer_ip>:9997

Enable receiving on indexer:
Settings → Forwarding and Receiving → Enable receiving

---

## 🛠️ Step 5: Verify Data Ingestion

Search in Splunk:
index=main

Check logs are visible ✅

---

## 🛠️ Step 6: Perform Log Analysis

Example Queries:

- Find errors:
  index=main ERROR

- Count logs:
  index=main | stats count

- Group by type:
  index=main | stats count by sourcetype

---

## ✅ Outcome

- Successfully configured Splunk components  
- Logs collected using forwarder  
- Logs indexed and stored  
- Data analyzed using SPL queries  

---

## 📘 Key Learnings

- Splunk setup involves multiple components  
- Proper configuration is critical  
- Log analysis helps in troubleshooting and monitoring
