# Basic-Network-Scanning-with-Nmap
# Task 1: Basic Network Scanning with Nmap

## Objective
To identify open TCP ports and services running on my own Windows computer using Nmap.

## Tools Used
- Windows 10/11
- Nmap 7.99
- Command Prompt

## Methodology
1. Verified the Nmap installation using `nmap --version`.
2. Ran a basic scan against `127.0.0.1`.
3. Ran a service-version scan using `nmap -sV`.
4. Identified open ports and reviewed their security implications.
5. Performed OS detection where supported.

## Findings

| Port | Service | Security consideration |
|---|---|---|
| 135/tcp | Microsoft Windows RPC | Restrict unnecessary remote access. |
| 445/tcp | Microsoft-DS / SMB | Restrict SMB access to trusted networks. |
| 3389/tcp | MS WBT Server / RDP | Restrict Remote Desktop access and use strong authentication. |

These ports were reported as open by the local scan. An open port does not automatically mean a vulnerability exists.

## Security Recommendations
- Keep Windows and installed software updated.
- Review Windows Firewall inbound rules.
- Disable unnecessary Remote Desktop and file-sharing services.
- Restrict access to services that are not required.
- Repeat scans after configuration changes.

## Evidence
- `screenshots/nmap_scan.png`
- `nmap_scan_results.txt`

## Ethical Considerations
This scan targeted my own computer using the loopback address `127.0.0.1`. Scanning other systems requires explicit authorization.

## Conclusion
Nmap helped identify listening services on the local Windows computer. Reviewing these services and limiting unnecessary access can reduce the system's attack surface.
