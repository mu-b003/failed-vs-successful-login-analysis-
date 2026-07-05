# Commands Used

## Check Network Configuration

```bash
ip a
```

Displays network interface information and assigned IP addresses.

---

## Check SSH Service Status

```bash
sudo systemctl status ssh
```

Verifies that the SSH service is running.

---

## Connect to the Target System

```bash
ssh IT-support@192.168.150.129
```

Creates SSH authentication events for analysis.

---

## Display Failed and Successful Login Events

```bash
sudo grep -E "Failed password|Accepted password" /var/log/auth.log
```

Extracts failed and successful SSH authentication events from the authentication log.

---

## Count Failed Login Attempts by Source IP

```bash
sudo grep -a "Failed password" /var/log/auth.log | awk '{for(i=1;i<=NF;i++) if($i=="from") print $(i+1)}' | sort | uniq -c | sort -nr
```

Counts failed SSH login attempts for each source IP address.

---

## Count Successful Login Attempts by Source IP

```bash
sudo grep -a "Accepted password" /var/log/auth.log | awk '{for(i=1;i<=NF;i++) if($i=="from") print $(i+1)}' | sort | uniq -c | sort -nr
```

Counts successful SSH login attempts for each source IP address.

---

# Investigation Outcome

The collected commands were used to verify SSH service availability, analyze authentication logs, identify failed and successful login attempts, determine the source IP address, and summarize authentication activity in a controlled laboratory environment.
