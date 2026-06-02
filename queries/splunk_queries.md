# Splunk Queries

## Find all errors
index=main ERROR

## Count errors
index=main ERROR | stats count

## Group logs by type
index=main | stats count by log_level

## Time-based search
index=main earliest=-24h
