# Failed vs Successful Login Analysis

## Overview

This project demonstrates how to analyze SSH authentication logs on a Linux system to identify and compare failed and successful login attempts. The investigation was performed in a controlled lab environment using Ubuntu as the target system and Kali Linux as the client.

The objective was to generate authentication events, examine the system logs, extract relevant security information, and distinguish between normal login activity and a high volume of failed authentication attempts.

---

## Objectives

* Analyze Linux SSH authentication logs.
* Identify failed login attempts.
* Identify successful login attempts.
* Extract source IP addresses.
* Count failed and successful login events.
* Detect authentication patterns that may indicate a brute-force attack.
* Practice basic SOC investigation techniques.

---

## Lab Environment

| Component      | Details                          |
| -------------- | -------------------------------- |
| Target System  | Ubuntu Linux                     |
| Client System  | Kali Linux                       |
| Service        | OpenSSH Server                   |
| Log File       | `/var/log/auth.log`              |
| Analysis Tools | grep, awk, sort, uniq, systemctl |

---

## Scenario

A user attempted to connect to the Ubuntu system through SSH.

The investigation included two authentication scenarios:

1. Manual SSH login with two failed password attempts followed by a successful login.
2. Multiple automated failed login attempts generated in a controlled lab environment to create authentication events for analysis.

The generated logs were examined to identify authentication outcomes, source IP addresses, and event frequency.

---

## Investigation Steps

* Verify that the SSH service is running.
* Generate SSH login attempts.
* Review authentication logs.
* Extract failed login events.
* Extract successful login events.
* Count authentication attempts by source IP.
* Compare failed and successful authentication activity.
* Document the findings.

---

## Key Findings

* SSH authentication logs successfully recorded both failed and successful login attempts.
* The source IP address responsible for the authentication attempts was identified.
* Multiple failed login attempts were detected before successful authentication.
* Authentication events were extracted and summarized using standard Linux command-line tools.
* The collected evidence demonstrates how authentication logs can support security investigations.

---

## Skills Demonstrated

* Linux Log Analysis
* SSH Authentication Analysis
* Authentication Monitoring
* Security Event Investigation
* Log Filtering
* Event Correlation
* Linux Command-Line Investigation
* Blue Team Fundamentals
* SOC Analyst Basics

---

## Commands Used

* `systemctl`
* `grep`
* `awk`
* `sort`
* `uniq`
* `ssh`

---

## Evidence

Project evidence is available in the **evidence/** directory and includes:

* SSH service status
* Manual login attempts
* Failed authentication events
* Successful authentication events
* Authentication summary screenshots

---

## Learning Outcome

This project demonstrates the ability to investigate Linux authentication logs, differentiate between failed and successful SSH login attempts, extract security-relevant information, and document findings using standard command-line tools in a controlled laboratory environment.

---

## Disclaimer

This project was conducted in a personal, isolated laboratory environment for educational and defensive cybersecurity purposes only. No unauthorized systems or third-party infrastructure were targeted during this exercise.
