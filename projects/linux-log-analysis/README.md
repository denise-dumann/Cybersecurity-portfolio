# Linux Log Analysis

## Objective
Learn how to inspect authentication logs and identify failed login attempts.

## Skills
- Linux command line
- Log analysis
- Basic incident investigation

## Lab Status
Planned

## Investigation Steps
1. Identify the relevant log file.
2. Review authentication events.
3. Search for failed login attempts.
4. Document findings and recommendations.

## Findings

### Summary
Multiple failed SSH login attempts were observed from a single source IP address, `192.0.2.10`. The activity is considered suspicious and requires further investigation.

### Evidence
- **Total failed login attempts:** 4
- **Attempts from `192.0.2.10`:** 3
- **Attempts from `192.0.2.15`:** 1
- **Usernames targeted by `192.0.2.10`:** `admin`, `test`, and `root`
- **Successful logins from `192.0.2.10` in the provided dataset:** None observed

### Assessment
The repeated failed login attempts and use of multiple usernames may indicate suspicious authentication activity. However, the available evidence is insufficient to confirm a brute-force attack or unauthorized access.

### Initial Investigation Priority
**Medium** — based on the limited evidence available in this training scenario. The priority may change after reviewing additional logs and the affected system's context.

### Recommended Next Steps
1. Review a broader time window to determine the frequency of failed login attempts.
2. Check for successful logins from the same source IP address across relevant log sources.
3. Investigate whether the attempted usernames correspond to valid accounts.
4. Correlate authentication logs with other security events.

### Limitations
This analysis uses synthetic log data created for educational purposes. The IP addresses and events do not represent a verified real-world security incident.
