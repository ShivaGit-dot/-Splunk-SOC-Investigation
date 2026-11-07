#  Splunk SOC Investigation Portfolio

 Hands-on Security Operations Center (SOC) | SIEM Analysis | Threat Hunting | Incident Investigation

##  Executive Summary

This repository showcases a practical Security Operations Center (SOC) investigation portfolio consisting of **5 hands-on cybersecurity investigation labs**.

The portfolio demonstrates practical blue team capabilities, including security log analysis, authentication monitoring, brute-force investigation, suspicious PowerShell execution analysis, endpoint process investigation, network traffic analysis, threat intelligence research, and incident documentation.

Using **Splunk Enterprise as the primary SIEM platform** and Wireshark for network traffic analysis, these investigations demonstrate the process of identifying suspicious activities, analyzing security events, correlating evidence, evaluating potential threats, and documenting investigation findings.

The final capstone investigation integrates SIEM-based endpoint analysis with network-level evidence and threat intelligence documentation to demonstrate a structured, multi-source SOC investigation workflow.

Each lab includes relevant datasets, documented SPL queries, investigation screenshots, dashboard evidence, and final investigation reports.

##  Toolset & Technologies

| Category | Tools & Technologies |
|---|---|
| SIEM & Log Analytics | Splunk Enterprise, Search Processing Language (SPL) |
| Network Analysis | Wireshark, TCP/IP, HTTP, TCP Stream Analysis |
| Threat Intelligence | MITRE ATT&CK, IOC Analysis, Threat Intelligence Research |
| Endpoint Investigation | Windows Event Logs, Process Creation Events, PowerShell Analysis |
| Data Analysis | Microsoft Excel, CSV Log Analysis |
| Virtualization | VMware, Kali Linux |
| Incident Response | Security Triage, Evidence Correlation, Incident Assessment, Remediation Recommendations |

## Primary Investigation Tools

**Splunk Enterprise**
- Security event monitoring and investigation.
- SPL query development.
- Event filtering and statistical analysis.
- Suspicious process and authentication analysis.
- Security dashboard development.

**Wireshark**
- Network packet inspection.
- TCP conversation analysis.
- HTTP request and response investigation.
- Network communication analysis.

**MITRE ATT&CK**
- Mapping observed activities to adversary tactics and techniques.
- Understanding suspicious execution behavior.
- Supporting investigation documentation.

##  SOC Investigation Methodology

The investigations follow a structured security investigation methodology:

| Phase | Investigation Activity |
|---|---|
| 01. Evidence Collection | Collect and examine relevant security logs and network evidence. |
| 02. Behavior Analysis | Identify suspicious patterns, processes, and authentication activities. |
| 03. Correlation | Correlate related events and supporting evidence. |
| 04. Assessment | Evaluate suspicious activities and determine potential security impact. |
| 05. MITRE ATT&CK Mapping | Map relevant adversary behaviors to ATT&CK techniques. |
| 06. Severity Classification | Assess investigation severity based on available evidence. |
| 07. Response | Document containment, mitigation, and remediation recommendations. |

**Investigation Workflow:**

Evidence → Behavior → Correlation → Assessment → MITRE ATT&CK → Severity → Response

##  Repository Structure

The repository is organized into five individual investigation projects.

Splunk-SOC-Investigation/
│
├── 01_Authentication & Brute-Force Investigation/
│   ├── Raw Dataset
│   ├── 02_Spl_Searches/
│   ├── 03_Screenshots/
│   ├── Dashboard Screenshot
│   └── 05_Final_Report/
│
├── 02_Suspicious PowerShell Investigation/
│   ├── Dataset
│   ├── Splunk Searches
│   ├── Screenshots
│   ├── Dashboard
│   └── Final Report
│
├── 03_Suspicious Office Document Investigation/
│   ├── Dataset
│   ├── Splunk Searches
│   ├── Screenshots
│   ├── Dashboard
│   └── Final Report
│
├── 04_Credential_Attack_Investigation/
│   ├── Dataset
│   ├── Splunk Searches
│   ├── Screenshots
│   ├── Dashboard
│   └── Final Report
│
├── 05_Comprehensive_Threat_Investigation/
│   ├── Dataset
│   ├── Splunk Searches
│   ├── 03_Screenshots/
│   │   ├── Splunk/
│   │   └── Wireshark/
│   ├── 04_Network_Analysis/
│   │   ├── Threat_Intelligence.txt
│   │   └── Wireshark_Data/
│   ├── 05_Dashboard/
│   └── 06_Investigation_Report/
│
└── README.md

*Note: Refer to individual lab directories for the actual filenames and complete folder contents.*

##  Lab Breakdown & Key Objectives

###  Lab 01: Authentication & Brute-Force Investigation

**Focus:** Windows authentication monitoring and brute-force investigation.

**Key Investigation Activities:**
- Analyzed Windows Security Event Logs.
- Investigated failed authentication attempts (Event ID 4625).
- Examined successful authentication events (Event ID 4624).
- Investigated suspicious login patterns.
- Compared failed and successful authentication activity.
- Examined source IP activity and targeted accounts.
- Developed Splunk searches and an authentication monitoring dashboard.

**Key Deliverables:**
- Raw authentication log dataset.
- Documented SPL search queries.
- Authentication investigation screenshots.
- Dashboard visualization.
- Final incident investigation report.
  
###  Lab 02: Suspicious PowerShell Investigation

**Focus:** PowerShell execution analysis and suspicious command-line investigation.

**Key Investigation Activities:**
- Investigated Windows process creation events (Event ID 4688).
- Analyzed PowerShell process execution.
- Examined encoded PowerShell command patterns.
- Investigated suspicious execution parameters.
- Analyzed process information and supporting event evidence.
- Developed Splunk searches for suspicious PowerShell activity.

**Key Deliverables:**
- PowerShell investigation dataset.
- SPL detection and investigation queries.
- Encoded command analysis evidence.
- Investigation dashboard.
- Final investigation documentation.

###  Lab 03: Suspicious Office Document & LOLBin Investigation

**Focus:** Suspicious Office document execution and Living-off-the-Land Binary (LOLBin) investigation.

**Key Investigation Activities:**
- Investigated suspicious macro-enabled Excel document activity.
- Analyzed process execution relationships.
- Investigated suspicious use of 'certutil.exe' and 'rundll32.exe'.
- Examined parent-child process relationships.
- Identified suspicious execution behavior.
- Correlated process activity with available security events.
- Mapped relevant findings to MITRE ATT&CK.

**Key Deliverables:**
- Office document investigation dataset.
- Splunk investigation queries.
- Process execution evidence.
- Investigation screenshots and dashboard.
- Final incident investigation report.

###  Lab 04: Credential Attack Investigation

**Focus:** Credential-related threat investigation and security event analysis.

**Key Investigation Activities:**
- Investigated credential-related security activity.
- Analyzed relevant Windows security events.
- Examined suspicious authentication and process-related evidence.
- Used SPL queries to filter and investigate security events.
- Correlated relevant findings.
- Assessed suspicious activity and documented investigation results.

**Key Deliverables:**
- Investigation dataset.
- Documented Splunk SPL queries.
- Investigation screenshots.
- Security monitoring dashboard.
- Final investigation report.

###  Lab 05: Comprehensive Multi-Source Threat Investigation

**Focus:** End-to-end threat investigation integrating Splunk SIEM, Wireshark network analysis, and threat intelligence research.

This capstone investigation demonstrates the correlation of endpoint telemetry and network-level evidence to reconstruct suspicious activity.

**Key Investigation Activities:**

**1. Splunk SIEM Investigation**
- Analyzed Windows process creation events.
- Investigated suspicious PowerShell execution.
- Examined process relationships and command-line arguments.
- Identified suspicious execution parameters.
- Investigated network-related activity in endpoint telemetry.
- Developed SPL queries for threat investigation.

**2. Wireshark Network Traffic Analysis**
- Examined TCP communication between lab endpoints.
- Investigated HTTP GET requests.
- Analyzed a simulated executable download request.
- Examined HTTP POST upload activity.
- Investigated TCP communication over port 8443.
- Examined packet-level evidence and reconstructed communication sequences.

**3. Threat Intelligence & IOC Investigation**
- Documented relevant investigation indicators.
- Examined network-related indicators.
- Performed threat intelligence research.
- Maintained investigation findings in 'Threat_Intelligence.txt'.

**4. Evidence Correlation**
- Correlated endpoint process activity with network evidence.
- Examined the relationship between suspicious execution and external communication.
- Reconstructed the investigation timeline.
- Evaluated the available evidence and potential security impact.

**5. Investigation Reporting**
- Documented investigation findings.
- Included relevant evidence and screenshots.
- Recorded network analysis observations.
- Documented MITRE ATT&CK mapping.
- Prepared investigation conclusions and response recommendations.

**Key Deliverables:**
- Investigation dataset.
- Advanced Splunk SPL queries.
- Splunk investigation screenshots.
- Wireshark packet analysis screenshots.
- Threat intelligence documentation.
- Network analysis artifacts.
- Comprehensive investigation dashboard.
- Final investigation report.

**Important:** The Lab 05 network artifacts use synthetic training traffic. They are intended for controlled cybersecurity investigation and learning purposes.

## 🎯 Core Competencies Demonstrated

### SIEM Operations & Threat Detection
- Splunk Enterprise operations.
- SPL query development.
- Security event filtering and analysis.
- Authentication monitoring.
- Suspicious process investigation.
- Dashboard development.

### Endpoint Security Investigation
- Windows Event Log analysis.
- Event ID 4624 and 4625 investigation.
- Process Creation Event ID 4688 analysis.
- PowerShell command-line investigation.
- Parent-child process analysis.
- LOLBin investigation.

### Network Security Analysis
- Wireshark packet inspection.
- TCP communication analysis.
- HTTP request and response analysis.
- Network evidence correlation.
- Network communication investigation.

### Threat Intelligence & Incident Response
- IOC identification and documentation.
- Threat intelligence research.
- MITRE ATT&CK mapping.
- Security incident assessment.
- Investigation timeline reconstruction.
- Incident reporting and remediation recommendations.
  
##  How to Navigate This Repository

1. Open any of the five investigation directories.
2. Review the dataset to understand the available security events.
3. Navigate to the Splunk Searches folder to examine the documented SPL queries.
4. Review the screenshots to understand the investigation process and supporting evidence.
5. Explore the dashboard evidence to examine the visualized security findings.
6. Open the Final Report to review the investigation conclusions and recommendations.


## 👨‍💻 Author & Contact

>> SHIVA GAUD

- **GitHub:** [ShivaGit-dot](https://github.com/ShivaGit-dot)
- **LinkedIn:** linkedin.com/in/shiva-gaud-57048a41b


### 📌 Disclaimer

This repository is intended for educational and cybersecurity training purposes.

All investigations were conducted using lab datasets and controlled environments. The documented findings represent the analysis of the available training evidence and should not be interpreted as confirmed real-world security incidents.
