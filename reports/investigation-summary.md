# Threat Intelligence Investigation Report

## 1. Executive Summary

This report documents a threat intelligence investigation conducted as part of a CyberDefenders Blue Team challenge involving suspicious activity at GlobalTech Industries.

The incident involved abnormal network traffic originating from multiple workstations. Employees reported that their search queries were being redirected to unfamiliar websites, raising concerns about potential malware activity.

The investigation focused on identifying the associated threat cluster, examining malware metadata, identifying additional malware components, and determining the reported command-and-control (C2) domain.

Using VirusTotal, Red Canary, Zscaler, and Google Search, six key findings were established.

The investigation identified the threat cluster as **Yellow Cockatoo**, an associated DLL filename, a dropped `.dat` file, two historical timestamps, and a reported C2 domain.

## 2. Incident Overview

| Field | Details |
|---|---|
| Organization | GlobalTech Industries (fictional scenario) |
| Investigation type | Threat Intelligence |
| Challenge platform | CyberDefenders |
| Primary concern | Suspicious search query redirection |
| Threat cluster | Yellow Cockatoo |
| Investigation status | Completed |

### Reported Symptoms

- Abnormal network traffic from multiple workstations.
- Employee search queries redirected to unfamiliar websites.
- Suspicion of malware-related activity.

## 3. Investigation Objectives

The investigation aimed to:

1. Identify the threat cluster associated with the malware sample.
2. Determine the malware's associated filename.
3. Establish its reported compilation timestamp.
4. Identify its first submission date to VirusTotal.
5. Identify additional files dropped in the Windows AppData directory.
6. Identify the reported C2 domain.

## 4. Tools and Intelligence Sources

| Tool / Source | Investigation Purpose |
|---|---|
| VirusTotal | Hash lookup, file metadata, timestamps, and behavioural analysis |
| Red Canary | Threat cluster identification |
| Zscaler | Malware component and behaviour research |
| Google Search | Initial SHA256 intelligence lookup |

## 5. Investigation Findings

### Finding 1: Threat Cluster Identification

**Result:** Yellow Cockatoo

The SHA256 hash supplied in `hash.txt` was searched using Google. The search results led to a Red Canary technical analysis identifying the associated threat cluster as Yellow Cockatoo.

### Finding 2: Malware Filename

**Result:** `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`

The SHA256 hash was submitted to VirusTotal. The associated filename was displayed in the file information.

### Finding 3: Reported Compilation Timestamp

**Result:** `2020-09-24 18:26`

The VirusTotal Details tab was examined. Under History, the Creation Time field displayed the reported timestamp.

### Finding 4: First VirusTotal Submission

**Result:** `2020-10-15 02:47`

The History section under the VirusTotal Details tab showed the First Submission timestamp.

### Finding 5: Dropped Malware Component

**Result:** `solarmarker.dat`

Zscaler threat intelligence information identified the `.dat` file associated with the malware and reported as being dropped in the Windows AppData directory.

### Finding 6: Command-and-Control Domain

**Result:** `gogohid.com`

The VirusTotal Behavior tab was examined to identify network indicators associated with the malware sample. The domain `gogohid.com` was identified as the reported C2 domain.

## 6. Indicators of Compromise

| Indicator Type | Identified Value |
|---|---|
| Threat cluster | Yellow Cockatoo |
| Malware filename | `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll` |
| Dropped file | `solarmarker.dat` |
| C2 domain | `gogohid.com` |
| SHA256 | Refer to original `hash.txt` |

**Note:** The original SHA256 value should be inserted from the supplied `hash.txt` file before this report is considered complete.

## 7. Timeline Analysis

The investigation identified two relevant timestamps from VirusTotal:

| Event | Date and Time |
|---|---|
| Reported file creation | 24 September 2020, 18:26 |
| First VirusTotal submission | 15 October 2020, 02:47 |

The timestamps are approximately 20 days and 8 hours apart.

These dates provide historical context for the malware sample. They do not establish when the malware was first developed, deployed, or executed within GlobalTech Industries.

## 8. Security Assessment

The investigation produced several indicators that can support further threat hunting and incident response activities.

The identified DLL filename and dropped `.dat` file provide starting points for endpoint searches. The reported C2 domain provides a network indicator that can be investigated through DNS, firewall, and proxy logs.

The threat cluster identification also provides a basis for further research into related threat intelligence reporting.

However, the available challenge findings do not independently establish the initial infection vector, successful C2 communication, persistence mechanism, or the number of compromised workstations.

Additional endpoint and network telemetry would be required to confirm the full extent of the incident.

## 9. Recommended Incident Response Actions

### Detection and Investigation

- Search endpoint telemetry for the identified DLL filename.
- Search Windows AppData directories for `solarmarker.dat`.
- Use the original SHA256 hash to identify matching files.
- Review DNS, proxy, and firewall logs for connections involving `gogohid.com`.
- Investigate suspicious processes and execution activity on affected workstations.

### Containment

- Validate the reported C2 domain and associated infrastructure.
- Apply appropriate DNS or web filtering controls if malicious activity is confirmed.
- Isolate confirmed compromised endpoints where necessary.
- Preserve relevant logs and forensic evidence.

### Eradication and Recovery

- Identify and remove confirmed malicious components.
- Investigate potential persistence mechanisms.
- Validate endpoint integrity before returning affected workstations to normal operation.
- Continue monitoring for related indicators.

## 10. Conclusion

This investigation demonstrated how publicly available threat intelligence resources can be used to investigate suspicious malware activity and collect indicators of compromise.

The analysis identified Yellow Cockatoo as the associated threat cluster and uncovered relevant malware metadata, a dropped file, and a reported C2 domain.

These findings provide a foundation for further endpoint investigation, threat hunting, and defensive monitoring.

The exercise strengthened practical skills in threat intelligence research, malware identification, IOC analysis, and incident response documentation.

## 11. References

- [CyberDefenders](https://cyberdefenders.org/)
- [VirusTotal](https://www.virustotal.com/)
- [Zscaler](https://www.zscaler.com/)
- [MITRE ATT&CK](https://attack.mitre.org/)

---

**Report Type:** Threat Intelligence Investigation  
**Organization:** GlobalTech Industries (fictional scenario)  
**Platform:** CyberDefenders  
**Status:** Completed
