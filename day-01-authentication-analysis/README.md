## 🧪 Day 01 — Authentication Log Analysis & Brute Force Detection

### 🎯 Objective
Analyze Linux SSH authentication logs to detect brute-force attempts and identify successful compromise patterns.

---

### 🧠 Scenario

Simulated attacker activity:

- Username enumeration (invalid user attempts)
- Password guessing (multiple failures)
- Successful login after repeated failures


### 🔍 Log Source

```bash
journalctl -u ssh
```

## 📸 Screenshots
![Brute Force Detection](./1.jpeg)
![Log Analysis](./2.jpeg)
![Splunk Dashboard](./3.jpeg)

## 🔍 Key Findings

- Multiple failed SSH login attempts detected (brute-force pattern)
- Same IP repeatedly attempting authentication
- Successful login after several failures indicates possible compromise

## 🛡️ Detection Logic

- Detect repeated failed logins
- Detect success after failures
- Track suspicious IP behavior

## 🚨 MITRE ATT&CK Mapping

- T1110 – Brute Force
- T1078 – Valid Accounts
