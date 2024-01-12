# Zyxel FLEX Series
---

## Version: **V1.0**

## Description

---

Created by Alen Stojkovic

Template description: **Zyxel Firewall FLEX Series by Alen Stojkovic**

## Overview

---

**Evaluierte Modelle:**

- Zyxel USG 60
- Zyxel FLEX 100 (Temp Sensoren funktionieren nicht, deaktivieren)
- Zyxel FLEX 200

## Author

---

Alen Stojkovic

## Items collected

---

| Item name | Description | Type |
| --- | --- | --- |
| ActiveSession usage | Anzahl akiver Sessions auf der ZyWALL | SNMP agent |
| CPU temperature | CPU Temperatur in Celsius | SNMP agent |
| CPU usage | Die CPU Auslastung in % | SNMP agent |
| DHCP Table | Auslesung der DHCP Tabelle | SNMP agent |
| FAN IC temperature | Lüfter Temperatur in Celsius | SNMP agent |
| FLASH usage | Die Speicher Auslastung in % | SNMP agent |
| hardware serial number | Die Hardware Seriennummer | SNMP agent |
| RAM usage | Die RAM Auslastung in % | SNMP agent |
| system version | Die Running Firmware | SNMP agent |

## Triggers

---

| Trigger | Description | Expression | Severity |
| --- | --- | --- | --- |
| High Active Sessions | Warnung bei überschreitung von 10.000 Sessions | last(/Zyxel Firewall FLEX Series by Alen/zyflex.activesessionusage)>10000 | High |
| High CPU | Wenn über 85% die Temperatur steigt | last(/Zyxel Firewall FLEX Series by Alen/zyflex.cpuutalization)>85 | High |

## Graph

---

| Graph | Function | on Item |
| --- | --- | --- |
| Active Session Usage | AVG | ActiveSession Usage |
| Hardware Monitoring | AVG | CPU, RAM & FLASH Usage |

## Discovery rules

---

| Name | Description | Type | Key and additional info |
| --- | --- | --- | --- |
| vpn discovery | VPN Monitoring | SNMP agent | vpn.discovery |
