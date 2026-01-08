## Web Reconnaissance Detection (Wazuh SIEM)
### Scenario Overview

* Configured Kali Linux as a monitored endpoint using Wazuh agent

* Generated suspicious web traffic by requesting multiple non-existent and sensitive URLs

* Observed correlated web events and rule triggers in Wazuh SIEM

* Performed SOC L1 investigation and escalated based on reconnaissance pattern

---
### Alert Details

* Alert Type: Web Anomaly / Web Reconnaissance

* Rule Description: Web server 400 error code

* Detection Source: Wazuh SIEM

* Affected System: Kali Linux endpoint

* Severity: Medium → High (correlation-based)

---
### Logs & Evidence

* Multiple HTTP requests to non-existent and sensitive paths such as /admin, /wp-admin, and random URLs

* High number of web error responses (404 / malformed requests) within a short time window

* Wazuh correlation rules elevated repeated low-level web anomalies into a higher-risk alert

<br>
<img width="1893" height="470" alt="Wazuh web reconnaissance events" src="https://github.com/user-attachments/assets/fd18a926-208d-4dc8-99ea-4cbc884b12b7" />

---
### Analysis

* Reviewed Apache web access logs collected by the Wazuh agent

* Identified a high frequency of requests to multiple non-existent and sensitive URLs within one minute

* Activity pattern indicates automated scanning or reconnaissance rather than normal user browsing

* No evidence of successful exploitation or application compromise observed

---
### Decision

* Escalated to SOC L2

* Due to repeated suspicious web requests, short time window, and reconnaissance-like behavior that could precede exploitation

---
### Analyst Notes

* Observed repeated HTTP requests to non-existent and sensitive paths within a one-minute window. Activity pattern is consistent with web reconnaissance or scanning behavior. No successful exploitation observed. Escalating for further investigation.

---
### Learning Outcome

* Gained hands-on experience detecting web reconnaissance activity using Wazuh SIEM

* Learned how SIEM correlation rules group multiple web anomalies into actionable alerts

* Practiced SOC L1 escalation decisions based on patterns and context rather than single events

* Improved analyst documentation skills for SOC handover and audit purposes
