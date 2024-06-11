# 🛡️🌐 SOC-Honeylab Homelab 🚀🔒
![322930551-ca6ef315-dcbf-4176-b90f-c46a6bbf0459](https://github.com/baileytoy/SOC-Honeynet/assets/172320876/ad0781e9-9c25-4784-9fdf-465a6503e14d)

## Introduction
In this project, I set up a mini honeynet in Azure, integrating log sources from various resources into a Log Analytics workspace. Microsoft Sentinel utilized this data to create attack maps, trigger alerts, and generate incidents. I initially measured security metrics in an unsecured environment for 24 hours, then implemented security controls to harden the environment. After another 24-hour measurement period, the results of these metrics highlighted the impact of the applied security controls. The metrics we'll discuss include:
- SecurityEvent (Windows Event Logs)
- Syslog (Linux Event Logs)
- SecurityAlert (Log Analytics Alerts Triggered)
- SecurityIncident (Incidents created by Sentinel)
- AzureNetworkAnalytics_CL (Malicious Flows allowed into our honeynet)

## 🔒 Architecture Before Hardening / Security Controls 🔒
![68747470733a2f2f692e696d6775722e636f6d2f614244776e4b622e6a7067](https://github.com/baileytoy/SOC-Honeynet/assets/172320876/3f5e896f-edda-4219-93da-841dca0b031a)

## 🔒 Architecture After Hardening / Security Controls 🔒
![68747470733a2f2f692e696d6775722e636f6d2f59514e613950702e6a7067](https://github.com/baileytoy/SOC-Honeynet/assets/172320876/4a602936-f517-493b-b766-738ee61ba345)

The architecture of the mini honeynet in Azure consists of the following components:

- Virtual Network (VNet)
- Network Security Group (NSG)
- Virtual Machines (2 windows, 1 linux)
- Log Analytics Workspace
- Azure Key Vault
- Azure Storage Account
- Microsoft Sentinel

In the initial metrics (BEFORE), all resources were deployed with direct internet exposure. The Virtual Machines had unrestricted access configured in both their Network Security Groups and built-in firewalls. Additionally, other resources were deployed with public endpoints visible to the internet, making private endpoints unnecessary

However, in the (AFTER) metrics, we implemented significant security enhancements. Network Security Groups were strengthened by allowing only traffic from designated admin workstations. Additionally, all other resources were protected by their built-in firewalls and further secured through the use of Private Endpoints.

## 🛡️ Microsoft Sentinel Before Hardening / Secruity Controls 🛡️


## 🛡️ Microsoft Sentinel After Hardening / Secruity Controls 🛡️
