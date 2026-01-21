# Lab: Gatekeeper (TryHackMe)
# Lab Report: Gatekeeper (eCPPT Preparation)

## Enumeration Phase
Target IP: [Metti l'IP della macchina qui]

### Nmap Scan
| Port | Service | Version |
|------|---------|---------|
| 135  | msrpc   | Microsoft Windows RPC |
| 139  | netbios-ssn | Microsoft Windows netbios-ssn |
| 445  | microsoft-ds | Windows 7 Professional 7601 Service Pack 1 microsoft-ds |
| 31337 | Elite? | Gatekeeper Service |

### Findings
Il servizio sulla porta **31337** sembra essere un binario personalizzato per Windows. Questo scenario è tipico dell'esame **eCPPT** per testare le capacità di exploit development e successivo pivoting.
