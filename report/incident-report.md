# Incident Report

## Incident Information

**Project:** Failed vs Successful Login Analysis

**Investigation Type:** Linux SSH Authentication Log Analysis

**Environment:** Controlled Lab

**Operating System:** Ubuntu Linux

**Service:** OpenSSH Server

**Log Source:** `/var/log/auth.log`

---

# Executive Summary

This investigation analyzed SSH authentication events recorded on a Linux system. The objective was to identify failed and successful login attempts, determine the source of authentication requests, and summarize authentication activity using standard Linux command-line tools.

The collected logs contained both normal user authentication and a large number of failed SSH login attempts generated within a controlled laboratory environment for educational purposes.

---

# Investigation Objectives

* Verify SSH service activity.
* Identify failed login attempts.
* Identify successful login attempts.
* Determine the source IP address.
* Count authentication events.
* Analyze authentication behavior.
* Document investigation findings.

---

# Investigation Timeline

1. Verified that the SSH service was running.
2. Generated manual SSH login attempts.
3. Reviewed authentication logs.
4. Extracted failed authentication events.
5. Extracted successful authentication events.
6. Counted failed login attempts.
7. Counted successful login attempts.
8. Summarized the authentication activity.

---

# Evidence Collected

* SSH service status
* SSH authentication logs
* Failed login events
* Successful login events
* Source IP address
* Authentication statistics

---

# Findings

* SSH authentication logs recorded both failed and successful login attempts.
* Authentication activity originated from a single source IP within the lab environment.
* Manual login attempts produced both failed and successful authentication events.
* A large number of failed login attempts were generated to simulate authentication activity for analysis.
* Authentication events were successfully extracted and summarized using Linux command-line tools.

---

# Conclusion

The investigation successfully demonstrated how Linux authentication logs can be used to identify failed and successful SSH login attempts, extract security-relevant information, and support basic security monitoring and incident investigation.

All activities were performed in a controlled laboratory environment for defensive cybersecurity training.
