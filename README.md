# Yellow Cockatoo Threat Intelligence Investigation

![Category](https://img.shields.io/badge/Category-Threat%20Intelligence-blue)
![Platform](https://img.shields.io/badge/Platform-CyberDefenders-red)
![Tools](https://img.shields.io/badge/Tools-VirusTotal%20%7C%20Zscaler%20%7C%20Red%20Canary-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

## Project Overview

This project documents a threat intelligence investigation conducted through a CyberDefenders Blue Team challenge.

The investigation focuses on suspicious network activity affecting multiple workstations at GlobalTech Industries. Employees reported that their search queries were being redirected to unfamiliar websites, raising concerns about a potential malware infection.

The objective was to investigate the malware sample, identify its associated threat cluster, examine its characteristics, establish relevant timestamps, identify dropped files, and uncover its command-and-control (C2) infrastructure.

Using VirusTotal, Red Canary, and Zscaler threat intelligence resources, I gathered indicators and documented findings relevant to incident response and threat investigation.

## Investigation Scenario

During a routine IT security check, GlobalTech Industries detected abnormal network traffic originating from multiple employee workstations.

Further investigation revealed that some employees' search queries were being redirected to unfamiliar websites.

This behaviour prompted an investigation into the suspected malware responsible for the activity.

The investigation focused on identifying the malware, understanding its characteristics, and gathering indicators of compromise (IOCs) that could support containment and remediation.

## Objectives

- Identify the threat cluster associated with the malware sample.
- Determine the malware's common filename.
- Investigate the malware's reported compilation timestamp.
- Establish when the sample was first submitted to VirusTotal.
- Identify additional files dropped by the malware.
- Discover the malware's command-and-control infrastructure.
- Document findings as actionable threat intelligence.

## Tools and Technologies

| Tool / Resource | Purpose |
|---|---|
| [VirusTotal](https://www.virustotal.com/) | Malware hash investigation, file details, timestamps, and behavioural analysis |
| [Red Canary](https://redcanary.com/) | Threat intelligence research and threat cluster identification |
| [Zscaler](https://www.zscaler.com/) | Threat intelligence research and malware behaviour information |
| Google Search | Initial threat intelligence research using the SHA256 hash |

## Investigation Methodology

### 1. Threat Cluster Identification

The SHA256 hash provided in `hash.txt` was searched using Google.

The search results led to a Red Canary technical analysis identifying the associated threat cluster.

**Finding:** Yellow Cockatoo

### 2. Malware Filename Identification

The SHA256 hash was submitted to VirusTotal.

The file information displayed the associated malware filename.

**Finding:** `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll`

### 3. Malware Compilation Timestamp

The VirusTotal Details tab was examined.

Under the History section, the Creation Time field provided the reported timestamp.

**Finding:** `2020-09-24 18:26`

### 4. First Submission to VirusTotal

The VirusTotal Details tab was revisited to examine the History section.

The First Submission timestamp indicated when the sample was initially uploaded to the platform.

**Finding:** `2020-10-15 02:47`

### 5. Identification of Dropped Files

Zscaler threat intelligence information was examined to identify additional components associated with the malware.

The investigation identified a `.dat` file dropped in the Windows AppData folder.

**Finding:** `solarmarker.dat`

### 6. Command-and-Control Infrastructure

The VirusTotal Behavior tab was examined to identify network indicators associated with the malware sample.

The investigation identified a suspicious domain reported as C2 infrastructure.

**Finding:** `gogohid.com`

## Key Investigation Findings

| # | Finding | Result |
|---|---|---|
| 1 | Threat cluster | Yellow Cockatoo |
| 2 | Common malware filename | `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll` |
| 3 | Reported creation timestamp | `2020-09-24 18:26` |
| 4 | First VirusTotal submission | `2020-10-15 02:47` |
| 5 | Dropped AppData file | `solarmarker.dat` |
| 6 | Reported C2 domain | `gogohid.com` |

## Timeline Analysis

The two timestamps obtained from VirusTotal provide a basic timeline for the malware sample.

| Event | Timestamp |
|---|---|
| Reported file creation | 24 September 2020, 18:26 |
| First VirusTotal submission | 15 October 2020, 02:47 |

The difference between these timestamps is approximately 20 days and 8 hours.

This provides useful historical context for the sample. However, the compilation timestamp does not necessarily represent the malware's actual development date, and its first VirusTotal submission does not establish when it first infected a system.

## Indicators of Compromise (IOCs)

The investigation identified the following indicators:

| IOC Type | Indicator |
|---|---|
| SHA256 | Original sample hash from `hash.txt` |
| Filename | `111bc461-1ca8-43c6-97ed-911e0e69fdf8.dll` |
| Dropped file | `solarmarker.dat` |
| Domain | `gogohid.com` |
| Threat cluster | Yellow Cockatoo |

**Note:** The original SHA256 value should be added to this table from `hash.txt` to make the IOC documentation complete.

## MITRE ATT&CK Relevance

The CyberDefenders challenge categorizes the investigation under:

- **Initial Access**
- **Execution**

The findings provide useful threat intelligence for investigating suspicious malware activity. However, the available findings alone do not establish the exact initial access or execution techniques used.

Further endpoint and network evidence would be required to map specific techniques and sub-techniques confidently.

Reference: [MITRE ATT&CK](https://attack.mitre.org/)

## Incident Response Recommendations

Based on the findings, the following defensive actions would support an investigation of potentially affected workstations:

1. **Search endpoints:** Look for the identified DLL filename and `solarmarker.dat` across affected workstations.
2. **Hash-based detection:** Use the original SHA256 hash to search endpoint telemetry and identify matching samples.
3. **Network investigation:** Review DNS and proxy logs for communications involving `gogohid.com`.
4. **Network containment:** Validate the domain and associated infrastructure before implementing DNS or web filtering blocks.
5. **Endpoint investigation:** Examine suspicious processes, persistence mechanisms, file paths, and execution events.
6. **Threat hunting:** Search historical endpoint and network telemetry for related indicators and suspicious activity.

## Skills Demonstrated

- Threat intelligence research
- Malware hash investigation
- VirusTotal analysis
- Threat cluster identification
- Malware metadata analysis
- IOC identification and documentation
- C2 infrastructure identification
- Incident response fundamentals
- Security research and investigation reporting

## Repository Structure

```text
Yellow-Cockatoo-Threat-Intelligence-Investigation/
│
├── README.md
│
├── investigation/
│   ├── question-01.md
│   ├── question-02.md
│   ├── question-03.md
│   ├── question-04.md
│   ├── question-05.md
│   └── question-06.md
│
├── screenshots/
│   ├── question-01.png
│   ├── question-02.png
│   ├── question-03.png
│   ├── question-04.png
│   ├── question-05.png
│   └── question-06.png
│
└── reports/
    └── investigation-summary.md
```

## References

- [CyberDefenders](https://cyberdefenders.org/)
- [VirusTotal](https://www.virustotal.com/)
- [Zscaler](https://www.zscaler.com/)
- [MITRE ATT&CK](https://attack.mitre.org/)

## Disclaimer

This project was completed for educational and defensive cybersecurity purposes as part of a CyberDefenders Blue Team challenge.

The findings are based on publicly available threat intelligence and the information provided within the challenge environment. They should not be interpreted as confirmation that any specific organization or workstation was compromised.

---

**Project Category:** Threat Intelligence  
**Platform:** CyberDefenders  
**Investigation Focus:** Yellow Cockatoo malware analysis and IOC identification
