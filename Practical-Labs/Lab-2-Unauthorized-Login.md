## Unauthorized Login Alert Analysis (Junior Security Analyst Intro - TryHackMe).



### Overview


This repository documents my learning from the [Junior Security Analyst Intro room on TryHackMe](https://tryhackme.com/room/jrsecanalystintrouxo?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=copy&sharerId=66ae5e8b243b63afc413148f). 
The room introduces the core concepts of a Security Operations Center (SOC), focusing on Junior Security Analyst Journey, Security Operations Center (SOC), and A Day in the Life of a Security Analyst.

---

### Alert Details
* Alert Name:- Unauthorized login attempts with Successful SSH login 
* Severity:- Critical (as reported by the detection rule)
* Source:- External IP address
* Frequency:- Multiple repeated login attempts within a short time window

---

### Logs Reviewed (EVIDENCE)
* Authentication logs related to SSH access
* Time window:- Jan 6th 2026 at 14:13
* Pattern observed: Repeated unauthorized login attempts from the same external IP

---

### Analysis

1. Why is this abnormal? <br>
A. Authentication logs showed a successful SSH login followed by multiple unauthorized login attempts from the same external IP address. This pattern does not match normal user behavior.

2. What makes it risky? <br>
A. The activity involved remote SSH access from an external IP. A successful login combined with repeated unauthorized attempts increases the risk of account compromise and potential impact on systems.

---

### Decision
* Action Taken: Escalated to SOC L2
* Reason: Evidence of abnormal authentication behavior involving external SSH access and repeated unauthorized attempts, indicating potential security risk.

---

### Learning Outcome
This case reinforced the importance of analyzing authentication logs with context and patterns. It highlighted how SOC L1 analysts rely on evidence and behavior analysis to make escalation decisions, while tools primarily assist in log visibility.

