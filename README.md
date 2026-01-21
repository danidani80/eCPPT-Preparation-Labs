# Lab Report: Gatekeeper (eCPPT Preparation)

## 1. Enumeration Phase
**Target IP:** `10.81.165.68`

### Nmap Scan Results
| Port | Service | Version |
|------|---------|---------|
| 135  | msrpc   | Microsoft Windows RPC |
| 139  | netbios-ssn | Microsoft Windows netbios-ssn |
| 445  | microsoft-ds | Windows 7 Professional 7601 SP1 |
| 3389 | rdp     | Microsoft Terminal Services |
| 31337| Elite?  | Gatekeeper Service (Vulnerable) |

> **Note:** L'OS Discovery conferma che il target è un sistema **Windows 7 Professional 7601 Service Pack 1**.

---

## 2. Exploitation Process (Buffer Overflow)
Per ottenere l'accesso iniziale, è stata identificata una vulnerabilità di tipo Buffer Overflow sul servizio Gatekeeper (Porta 31337).

1. **Fuzzing**: Il servizio crasha inviando un buffer di circa **200 byte**.
2. **Offset**: Identificato l'offset esatto a **146 byte** per il controllo del registro EIP.
3. **EIP Control**: Verificato il controllo del flusso di esecuzione sovrascrivendo l'EIP con l'indirizzo `0x080414c3` (JMP ESP).
4. **Payload**: Generato shellcode personalizzato con `msfvenom` (LHOST=192.168.137.88) escludendo i bad chars (`\x00`).

## 3. Final Result
Esecuzione dell'exploit finale e ricezione di una **Reverse Shell** come utente di sistema.
