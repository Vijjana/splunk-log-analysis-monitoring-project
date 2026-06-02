# Splunk Architecture

## Components:

### Forwarder
- Installed on source system
- Collects logs and sends to indexer

### Indexer
- Receives log data
- Stores and indexes logs

### Search Head
- Used for searching logs
- Provides dashboard and visualization

## Flow:
System Logs → Forwarder → Indexer → Search Head
