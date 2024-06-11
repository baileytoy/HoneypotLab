# SOC-Honeylab Homelab 🚀🔒
![322930551-ca6ef315-dcbf-4176-b90f-c46a6bbf0459](https://github.com/baileytoy/SOC-Honeynet/assets/172320876/ad0781e9-9c25-4784-9fdf-465a6503e14d)

## Introduction
In this project, I set up a mini honeynet in Azure, integrating log sources from various resources into a Log Analytics workspace. Microsoft Sentinel utilized this data to create attack maps, trigger alerts, and generate incidents. I initially measured security metrics in an unsecured environment for 24 hours, then implemented security controls to harden the environment. After another 24-hour measurement period, the results of these metrics highlighted the impact of the applied security controls. The metrics we'll discuss include:
- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)
