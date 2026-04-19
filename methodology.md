# Methodology

## Phase 1: Reconnaissance
- Identified target system in local network
- Verified connectivity using ping

## Phase 2: Enumeration
- Scanned open ports using Nmap
- Identified SMB services running on ports 139/445

## Phase 3: Exploitation
- Used Metasploit module: usermap_script
- Configured payload reverse shell
- Gained remote shell access

## Phase 4: Post Exploitation
- Collected system information (whoami, id, hostname)
- Verified system compromise

## Phase 5: Incident Response Simulation
- Detected unauthorized access
- Identified attack vector
- Contained session
- Recommended mitigation steps
