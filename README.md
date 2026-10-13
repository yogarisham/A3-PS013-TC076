# PS-013: Incident Timeline and Evidence Collection for Small Teams

## 1. Project Overview
This project aims to develop a lightweight tool that collects authorized log files, preserves their originals, calculates cryptographic hashes, normalizes timestamps, and creates a searchable incident timeline.

**Hackathon:** AIORI 3  
**Problem Statement:** PS-013 — Incident Timeline and Evidence Collection for Small Teams  
**Project Status:** Proposed / In Development / Prototype / Tested — update to reflect the actual status.

## 2. Problem
Incident responders often need to manually examine logs from different systems, formats, time zones, and clock settings. This project aims to organize those records into a traceable chronological timeline.

## 3. Objectives
- Process at least two text-log formats.
- Preserve original records and create normalized event records.
- Calculate SHA-256 hashes for collected files.
- Normalize timestamps to UTC where the required time-zone information is available.
- Flag timestamp uncertainty and possible clock skew.
- Identify and document parsing gaps.
- Support timeline search and incident-summary export.
- Evaluate the tool using three synthetic scenarios.
- Compare tool-assisted triage time with a documented manual baseline.

## 4. Proposed Workflow
Log ingestion → Evidence hashing → Parsing → Timestamp normalization → Timeline creation → Search and report → Evaluation.

## 5. Technology Stack
- Python
- Python standard library for hashing, regular expressions and timestamp processing
- SQLite or another lightweight storage option, if required
- Streamlit, if a web-based interface is implemented
- pytest or unittest for testing

## 6. Test Scenarios
1. Web access-log scenario.
2. Linux syslog-style service-event scenario.
3. Mixed time-zone / simulated clock-skew scenario with a malformed line.

## 7. Project Structure
Describe the purpose of the source-code, tests, synthetic data, documentation and evaluation folders.

## 8. Installation and Usage
Add verified setup commands, configuration instructions, and the exact command used to run the application.

## 9. Testing and Evaluation
Document test procedures and actual results, including hash verification, event coverage, parsing gaps, timestamp accuracy and triage time. Do not publish unmeasured performance claims.

## 10. Limitations
Document unsupported formats, uncertain timestamps, parser limitations and the need for human review.

## 11. References
- NIST SP 800-86: Guide to Integrating Forensic Techniques into Incident Response — https://csrc.nist.gov/pubs/sp/800/86/final

## 12. Responsible Use
Use synthetic logs or evidence from systems for which collection is authorized. Do not commit credentials, personal data or confidential incident evidence.
