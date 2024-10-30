# **Custom SIEM Solution for Virtual Space Industries Using Splunk**

## **Introduction**

This project involves the development and analysis of a custom Security Information and Event Management (SIEM) solution using Splunk to protect the fictional organization, Virtual Space Industries (VSI), against cyberattacks from a competitive rival, JobeCorp. Acting as a SOC analyst at Fable CyberSecurity Inc., I was tasked with monitoring critical VSI systems, including Windows servers and an Apache web server. The project demonstrates my proficiency in security monitoring, log analysis, threat detection, and incident response using Splunk.

## **Table of Contents**

- [Project Overview](#project-overview)
  - [Objectives](#objectives)
  - [Tools and Technologies](#tools-and-technologies)
- [Implementation Phases](#implementation-phases)
  - [Phase 1: Designing the SIEM Environment](#phase-1-designing-the-siem-environment)
  - [Phase 2: Configuring Data Inputs and Dashboards](#phase-2-configuring-data-inputs-and-dashboards)
  - [Phase 3: Attack Analysis and Incident Response](#phase-3-attack-analysis-and-incident-response)
- [Results and Findings](#results-and-findings)
- [Recommendations](#recommendations)
- [Conclusion and Reflections](#conclusion-and-reflections)
- [Contact Information](#contact-information)
- [License](#license)

## **Project Overview**

### **Objectives**

- **Design a Security Monitoring Environment**: Develop a Splunk-based SIEM solution to establish baselines, detect anomalies, and respond to cyber threats.
- **Monitor Critical Systems**: Collect and analyze logs from Windows servers and an Apache web server.
- **Detect and Analyze Attacks**: Identify and investigate simulated cyberattacks to assess the effectiveness of the SIEM.
- **Provide Recommendations**: Suggest improvements to enhance VSI's security posture based on analysis findings.

### **Tools and Technologies**

- **Splunk Enterprise**
- **Splunk Apps and Add-ons**:
  - **Splunk Add-on for Microsoft Windows**
  - **Splunk App for Windows Infrastructure**
- **Operating Systems**:
  - **Windows Server 2019**
  - **Ubuntu Server (Apache Web Server)**
- **Other Tools**:
  - **Wireshark**
  - **Python (for any scripts)**
  - **Visualization Tools** (for dashboards and reports)

For detailed reports and findings, please refer to the [SIEM Implementation Report](reports/SIEM_Implementation_Report.md).

## **Implementation Phases**

### **Phase 1: Designing the SIEM Environment**

- **Set Up Splunk Environment**:
  - Installed Splunk Enterprise on a dedicated server.
  - Configured Splunk to receive data from VSI's Windows servers and Apache web server.
- **Data Onboarding**:
  - Installed necessary Splunk forwarders on Windows and Linux servers.
  - Configured inputs to collect security logs, application logs, and system logs.
- **Baseline Establishment**:
  - Monitored normal system activity over a period to establish baseline metrics.
  - Identified patterns in log data to differentiate between regular operations and anomalies.

### **Phase 2: Configuring Data Inputs and Dashboards**

- **Windows Logs Monitoring**:
  - Collected Security, Application, and System logs.
  - Focused on events like logon attempts, account management, and policy changes.
- **Apache Web Server Monitoring**:
  - Ingested access logs and error logs.
  - Analyzed HTTP request methods, response codes, and traffic sources.
- **Dashboard Creation**:
  - Developed custom dashboards for real-time monitoring.
  - Visualized key metrics such as failed login attempts, unusual HTTP requests, and traffic spikes.
- **Alert Configuration**:
  - Set up alerts for critical events like multiple failed logins, account lockouts, and high volumes of 404 errors.
  - Tuned alert thresholds based on baseline data to minimize false positives.

### **Phase 3: Attack Analysis and Incident Response**

- **Simulated Cyberattacks**:
  - An attack was simulated by JobeCorp, targeting VSI's infrastructure.
  - Attacks included brute-force login attempts, SQL injection attempts, and DoS attacks.
- **Detection and Analysis**:
  - Used Splunk dashboards to detect anomalies during the attack period.
  - Investigated specific events, correlating data across different log sources.
- **Incident Response**:
  - Documented the incident timeline.
  - Analyzed attacker behavior and techniques.
  - Assessed the effectiveness of existing security controls.

## **Results and Findings**

- **Successful Detection of Attacks**:
  - Detected multiple brute-force login attempts on Windows servers.
  - Identified a spike in POST requests indicating possible SQL injection attempts.
  - Noted unusual traffic patterns and high error rates on the Apache server.
- **Analysis Insights**:
  - Attackers attempted to exploit weak passwords and unpatched vulnerabilities.
  - The source of attacks was traced to specific IP addresses associated with JobeCorp.
  - Existing alert thresholds were effective in highlighting critical events.

Detailed analysis is documented in the [Attack Analysis Report](reports/Attack_Analysis.md).

## **Recommendations**

- **Enhance Password Policies**:
  - Enforce stronger password requirements and implement multi-factor authentication.
- **Implement Geo-Blocking**:
  - Restrict access from non-essential geographic locations.
- **Update and Patch Systems**:
  - Regularly update systems to protect against known vulnerabilities.
- **Refine Alert Thresholds**:
  - Continuously adjust alert settings based on evolving threat patterns.
- **Improve Incident Response Plan**:
  - Develop a comprehensive incident response plan with clear procedures.

For a full list of recommendations, see [Recommendations](reports/Recommendations.md).

## **Conclusion and Reflections**

This project demonstrated the critical role of SIEM solutions in detecting and responding to cyber threats. By leveraging Splunk's capabilities, I was able to effectively monitor VSI's systems, detect simulated attacks, and provide actionable recommendations. The experience reinforced the importance of continuous monitoring, proper configuration, and proactive security measures.
