┌──(dani㉿vbox)-[~]
└─$ cat nmap_gatekeeper.md
┌──(dani㉿vbox)-[~]
└─$ nmap -sV -sC -Pn -p 135,139,445,31337,3389 10.81.165.68
Starting Nmap 7.95 ( https://nmap.org ) at 2026-01-21 23:06 CET
Stats: 0:00:11 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 20.00% done; ETC: 23:07 (0:00:24 remaining)
Stats: 0:00:44 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:07 (0:00:10 remaining)
Stats: 0:00:54 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:07 (0:00:12 remaining)
Stats: 0:01:02 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:07 (0:00:14 remaining)
Stats: 0:01:12 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:08 (0:00:17 remaining)
Stats: 0:01:22 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:08 (0:00:19 remaining)
Stats: 0:01:58 elapsed; 0 hosts completed (1 up), 1 undergoing Service Scan
Service scan Timing: About 80.00% done; ETC: 23:08 (0:00:28 remaining)
Stats: 0:02:56 elapsed; 0 hosts completed (1 up), 1 undergoing Script Scan
NSE Timing: About 99.86% done; ETC: 23:09 (0:00:00 remaining)
Nmap scan report for 10.81.165.68
Host is up (0.072s latency).

PORT      STATE SERVICE      VERSION
135/tcp   open  msrpc        Microsoft Windows RPC
139/tcp   open  netbios-ssn  Microsoft Windows netbios-ssn
445/tcp   open  microsoft-ds Windows 7 Professional 7601 Service Pack 1 microsoft-ds (workgroup: WORKGROUP)
3389/tcp  open  tcpwrapped
|_ssl-date: 2026-01-21T22:09:18+00:00; -15s from scanner time.
| rdp-ntlm-info: 
|   Target_Name: GATEKEEPER
|   NetBIOS_Domain_Name: GATEKEEPER                                                                                                                                                                                                        
|   NetBIOS_Computer_Name: GATEKEEPER                                                                                                                                                                                                      
|   DNS_Domain_Name: gatekeeper                                                                                                                                                                                                            
|   DNS_Computer_Name: gatekeeper                                                                                                                                                                                                          
|   Product_Version: 6.1.7601                                                                                                                                                                                                              
|_  System_Time: 2026-01-21T22:09:03+00:00                                                                                                                                                                                                 
| ssl-cert: Subject: commonName=gatekeeper                                                                                                                                                                                                 
| Not valid before: 2026-01-20T22:05:17                                                                                                                                                                                                    
|_Not valid after:  2026-07-22T22:05:17                                                                                                                                                                                                    
31337/tcp open  Elite?                                                                                                                                                                                                                     
| fingerprint-strings:                                                                                                                                                                                                                     
|   FourOhFourRequest:                                                                                                                                                                                                                     
|     Hello GET /nice%20ports%2C/Tri%6Eity.txt%2ebak HTTP/1.0                                                                                                                                                                              
|     Hello
|   GenericLines: 
|     Hello 
|     Hello
|   GetRequest: 
|     Hello GET / HTTP/1.0
|     Hello
|   HTTPOptions: 
|     Hello OPTIONS / HTTP/1.0
|     Hello
|   Help: 
|     Hello HELP
|   Kerberos: 
|     Hello !!!
|   LDAPSearchReq: 
|     Hello 0
|     Hello
|   LPDString: 
|     Hello 
|     default!!!
|   RTSPRequest: 
|     Hello OPTIONS / RTSP/1.0
|     Hello
|   SIPOptions: 
|     Hello OPTIONS sip:nm SIP/2.0
|     Hello Via: SIP/2.0/TCP nm;branch=foo
|     Hello From: <sip:nm@nm>;tag=root
|     Hello To: <sip:nm2@nm2>
|     Hello Call-ID: 50000
|     Hello CSeq: 42 OPTIONS
|     Hello Max-Forwards: 70
|     Hello Content-Length: 0
|     Hello Contact: <sip:nm@nm>
|     Hello Accept: application/sdp
|     Hello
|   SSLSessionReq, TLSSessionReq, TerminalServerCookie: 
|_    Hello
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port31337-TCP:V=7.95%I=7%D=1/21%Time=69714DF9%P=x86_64-pc-linux-gnu%r(G
SF:etRequest,24,"Hello\x20GET\x20/\x20HTTP/1\.0\r!!!\nHello\x20\r!!!\n")%r
SF:(SIPOptions,142,"Hello\x20OPTIONS\x20sip:nm\x20SIP/2\.0\r!!!\nHello\x20
SF:Via:\x20SIP/2\.0/TCP\x20nm;branch=foo\r!!!\nHello\x20From:\x20<sip:nm@n
SF:m>;tag=root\r!!!\nHello\x20To:\x20<sip:nm2@nm2>\r!!!\nHello\x20Call-ID:
SF:\x2050000\r!!!\nHello\x20CSeq:\x2042\x20OPTIONS\r!!!\nHello\x20Max-Forw
SF:ards:\x2070\r!!!\nHello\x20Content-Length:\x200\r!!!\nHello\x20Contact:
SF:\x20<sip:nm@nm>\r!!!\nHello\x20Accept:\x20application/sdp\r!!!\nHello\x
SF:20\r!!!\n")%r(GenericLines,16,"Hello\x20\r!!!\nHello\x20\r!!!\n")%r(HTT
SF:POptions,28,"Hello\x20OPTIONS\x20/\x20HTTP/1\.0\r!!!\nHello\x20\r!!!\n"
SF:)%r(RTSPRequest,28,"Hello\x20OPTIONS\x20/\x20RTSP/1\.0\r!!!\nHello\x20\
SF:r!!!\n")%r(Help,F,"Hello\x20HELP\r!!!\n")%r(SSLSessionReq,C,"Hello\x20\
SF:x16\x03!!!\n")%r(TerminalServerCookie,B,"Hello\x20\x03!!!\n")%r(TLSSess
SF:ionReq,C,"Hello\x20\x16\x03!!!\n")%r(Kerberos,A,"Hello\x20!!!\n")%r(Fou
SF:rOhFourRequest,47,"Hello\x20GET\x20/nice%20ports%2C/Tri%6Eity\.txt%2eba
SF:k\x20HTTP/1\.0\r!!!\nHello\x20\r!!!\n")%r(LPDString,12,"Hello\x20\x01de
SF:fault!!!\n")%r(LDAPSearchReq,17,"Hello\x200\x84!!!\nHello\x20\x01!!!\n"
SF:);
Service Info: Host: GATEKEEPER; OS: Windows; CPE: cpe:/o:microsoft:windows

Host script results:
|_clock-skew: mean: 59m45s, deviation: 2h14m10s, median: -15s
| smb2-security-mode: 
|   2:1:0: 
|_    Message signing enabled but not required
| smb-security-mode: 
|   account_used: guest
|   authentication_level: user
|   challenge_response: supported
|_  message_signing: disabled (dangerous, but default)
|_nbstat: NetBIOS name: GATEKEEPER, NetBIOS user: <unknown>, NetBIOS MAC: 02:f2:70:2e:5b:c9 (unknown)
| smb-os-discovery: 
|   OS: Windows 7 Professional 7601 Service Pack 1 (Windows 7 Professional 6.1)
|   OS CPE: cpe:/o:microsoft:windows_7::sp1:professional
|   Computer name: gatekeeper
|   NetBIOS computer name: GATEKEEPER\x00
|   Workgroup: WORKGROUP\x00
|_  System time: 2026-01-21T17:09:03-05:00
| smb2-time: 
|   date: 2026-01-21T22:09:03
|_  start_date: 2026-01-21T22:05:16

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 181.72 seconds
### Exploitation Process (Buffer Overflow)
Per ottenere l'accesso iniziale, è stata identificata una vulnerabilità di tipo Buffer Overflow sul servizio Gatekeeper (Porta 31337).

1. **Fuzzing**: Il servizio crasha inviando un buffer di circa 200 byte.
2. **Offset**: Identificato l'offset esatto a **146 byte** per il controllo del registro EIP.
3. **EIP Control**: Verificato il controllo del flusso di esecuzione sovrascrivendo l'EIP con l'indirizzo `0x080414c3` (JMP ESP).
4. **Payload**: Generato shellcode personalizzato con `msfvenom` (LHOST=192.168.137.88) escludendo i bad chars (`\x00`).

### Final Result
Esecuzione dell'exploit finale e ricezione di una Reverse Shell come utente di sistema.

