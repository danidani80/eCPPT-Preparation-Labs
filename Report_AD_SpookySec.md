# 🛡️ Rapporto Tecnico: Compromissione Active Directory
**Analista:** Daniel Marceddu | **Certificazione:** eCCPT v3 Prep

## 🛠️ Tecniche Utilizzate
- **Enumerazione**: CrackMapExec per identificazione utenti.
- **Accesso**: AS-REP Roasting (GetNPUsers.py) per estrazione hash.
- **PrivEsc**: Secretsdump per dumping NTDS.dit.
- **Post-Exploit**: Pass-the-Hash tramite Evil-WinRM.

## 🚩 Flag
- **Root**: TryHackMe{4ctiveD1rectoryM4st3r}
