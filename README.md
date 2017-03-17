# TA-cisco_firepower


## CIM compliant Cisco Firepower TA for Splunk

### CIM models
* Network Traffic
* Web

### Installation
1. Use FMC and configure your Firepower appliances to log Access Rules, IPS rules, DNS rules etc to your Splunk/Syslog server
2. Set the input with sourcetype "syslog" or sourcetype "cisco:firepower:syslog"

### Current limitations
* No session ID in events. Not sure how to get this from Firepower
* No duration field in events (this will have to be calculated with the delta of Start end End events)
* Does not support the Audit DM - TODO