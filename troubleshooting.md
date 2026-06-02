# 🔍 Splunk Troubleshooting Guide

## 📌 Overview
This document explains common issues encountered while working with Splunk and how they are resolved.

---

## ❗ Issue 1: Logs not showing in Search Head

### Cause:
- Forwarder not sending data
- Network issue between forwarder and indexer

### Solution:
- Check forwarder status
- Verify connection to indexer
- Restart Splunk services

---

## ❗ Issue 2: No data found in search results

### Cause:
- Incorrect index or time range
- Typo in search query

### Solution:
- Verify index name
- Adjust time picker (Last 24 hours)
- Check SPL query syntax

---

## ❗ Issue 3: High indexing delay

### Cause:
- Large volume of incoming logs
- Resource limitation

### Solution:
- Increase system resources (CPU / Memory)
- Optimize log ingestion settings

---

## ❗ Issue 4: Duplicate logs

### Cause:
- Same log file monitored multiple times
- Misconfigured forwarder

### Solution:
- Check inputs.conf
- Remove duplicate configurations

---

## 📘 Key Learnings

- Monitoring is not only searching logs
- Debugging issues is critical in real projects
- Splunk requires proper configuration at each layer (Forwarder, Indexer, Search Head)
