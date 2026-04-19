# Incident Response Report

## Detection
Unauthorized remote shell access detected on target system via SMB exploit.

## Impact
- Full remote command execution achieved
- System integrity compromised

## Containment
- Terminated active shell sessions
- Stopped Samba service

## Eradication
- Identified vulnerable service (SMB)
- Recommended patching and disabling unused services

## Recovery
- System restored to stable state
- Monitoring recommended for future attacks

## Lessons Learned
- SMB vulnerabilities are high risk
- Default configurations are unsafe
- Regular patching is critical
