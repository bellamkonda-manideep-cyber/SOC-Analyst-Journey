## Unauthorized Login Alert Analysis (Junior Security Analyst Intro - TryHackMe).

<br>

### Overview

<br>

This repository documents my learning from the [Junior Security Analyst Intro room on TryHackMe](https://tryhackme.com/room/jrsecanalystintrouxo?utm_campaign=social_share&utm_medium=social&utm_content=room&utm_source=copy&sharerId=66ae5e8b243b63afc413148f). 
The room introduces the core concepts of a Security Operations Center (SOC), focusing on Junior Security Analyst Journey, Security Operations Center (SOC), and A Day in the Life of a Security Analyst.

<br>

### Alert Details
* Alert Name:- Unauthorized login attempts and one Successful SSH login from the suspicious IP
* Severity:- Critical
* From:- External IP
* Frequency:- Malicious - Involved in 4 Cyber Attacks

<br>

### Logs Reviewed (EVIDENCE)
* Authentication logs:- Malicious - Involved in 4 Cyber Attacks
* Time window:- Jan 6th 2026 at 14:13
* Pattern:- Repeated

<br>

### Analysis

1. Why is this abnormal?
A. Observed the authentication logs Successful SSH login from the suspicious IP followed by Unauthorized login attempts from same IP address.

2. What makes it risky?
A. Successful SSH login from suspicious IP.

<br>

### Decision
* Escalated to L2:- Observed the authentication logs and found Successful SSH login which impacts on business.

<br>

### Learning Outcome
* After completing this lab from TryHackMe, I gained hands-on experince on A Day in the Life of a Security Analyst.


