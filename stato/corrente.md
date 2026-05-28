# Stato Corrente — Studio Attivo
**Sessione**: 27 | **Aggiornato**: 2026-05-27

> **Istruzione per Claude**: questo file va letto ALL'INIZIO di ogni sessione. È l'unico file obbligatorio per avere contesto.
> Per dettagli sui moduli (materiali, concetti, esercizi): `stato/percorso.md`
> Per lo storico delle sessioni passate: `stato/log_sessioni.md`
> Per il piano fasi e stime ore: `ESAMI SCELTI.md`

---

## Stato Moduli

### SysAdmin — Lab Amministrazione di Sistemi T
| Modulo | Nome | Stato | Note |
|--------|------|-------|------|
| 0A | Filesystem e Comandi Base | ✅ | Sessione 3 |
| 0B | Pipe, Redirect e Filtri | ✅ | Sessione 4 |
| 1A | Variabili, Condizioni, Loop | ✅ | Sessione 5 |
| 1B | Funzioni, Case, Test | ✅ | Sessione 6 |
| 2A | Gestione Utenti e Permessi | ✅ | Sessione 7-8 |
| 2B | LAB Utenti, Permessi e File | ✅ | |
| 2C | Gestione File: find, tar, rsync | ✅ | |
| 3A | Gestione Servizi con Systemd | ✅ | Sessione 10 |
| 3B | Gestione Pacchetti Software | ✅ | Sessione 13 |
| 3C | Gestione Processi | ✅ | Sessione 16 |
| 3D | Networking di Base | 🔄 | Es. 1 ✅; Es. 2-6 ⬜ |
| 3E | Vagrant Multi-Machine | ⬜ | |
| 3F | Automazione con Ansible | ⬜ | |

**Esercizi Scripting** (traccia parallela in `esercizi/`):
- Catena A — ls ricorsivo: lab_01 ⬜, lab_02 ⬜, lab_03 ⬜, es_03 ⬜
- Catena B — conversione tempo: lab_04 ⬜, lab_05 ⬜, lab_06 ⬜, lab_07 ⬜, es_04 ⬜
- Catena C — processi e segnali: es_05 ⬜, es_06 ⬜, es_07 ⬜, es_08 ⬜

### Security — Lab Sicurezza Informatica T
| Modulo | Nome | Stato | Note |
|--------|------|-------|------|
| S1 | Offensive Security + Enumerazione | 🔄 | Lezione pronta, LAB VM non eseguito |
| S2 | Autenticazione | ⬜ | |
| S3 | Web Security + LAB | ⬜ | |
| S4 | Binary Exploits + LAB Bruteforcing | ⬜ | |
| S5 | Firewall + LAB | ⬜ | |
| S6 | Sicurezza Fisica e Cloud | ⬜ | |
| S7 | LAB Backdoor Injection | ⬜ | |
| S8 | LAB Individuare e Filtrare Attacchi | ⬜ | |
| S9 | Demoni di Sistema + Autorizzazione | ⬜ | |
| S10 | Rilevare Attacchi + LAB NIDS Suricata | ⬜ | |
| S11 | Host-Based IDS + LAB Misconfiguration | ⬜ | |
| S12 | Sicurezza delle Comunicazioni | ⬜ | |

### Diritto — Diritto dell'Informatica T
| Modulo | Nome | Stato | Note |
|--------|------|-------|------|
| D1 | Concetti Giuridici di Base | ✅ | Sessione 11 |
| D2 | Ricerca e Analisi Fonti | ✅ | Sessione 12 |
| D3 | Diritto d'Autore e Software | ✅ | Sessione 16 |
| D4 | Banche Dati e Siti Web | ✅ | Sessione 21 |
| D5 | Contratti Informatici | ✅ | Sessione 22 |
| D6 | Contratto Sviluppo Software | ✅ | Sessione 24 |
| D7 | Proprietà Industriale | ✅ | Sessione 25 |
| D8 | Privacy e GDPR | ✅ | Sessione 26 |
| D9 | Firme Elettroniche | ✅ | Sessione 28 — ripasso 2/5 corrette, lacuna su gerarchia firme e opponibilità PEC |
| D10 | Commercio Elettronico | 🔄 | Lezione pronta |
| D11 | Reati Informatici | ⬜ | |
| D12 | AI Act | ⬜ | |
| D13 | DSA/DMA/Data Act | ⬜ | |

---

## Avanzamento

```
SysAdmin  ████████░░  77%  (10/13 moduli ✅)
Security  ░░░░░░░░░░   0%  (0/12 moduli ✅)
Diritto   ██████░░░░  62%  (8/13 moduli ✅)
```

---

## Prossimi Passi

> 🚨 **Urgenza Diritto**: D9 autoverifica + D10 grezzi+appunti + D11 + D12 + D13 = **5 step in 20 giorni** (esame 16/06). Ritmo necessario: ~1 modulo ogni 4 giorni. Nessun margine.

**Diritto** → D9: rispondere alle 5 domande di autoverifica → ✅ → D10: lezione pronta, scrivere appunti grezzi → `/appunti D10`
**SysAdmin** → 3D Es. 2-6: avviare VM, eseguire ping, ss -tlnp, /etc/hosts, dig, tcpdump → poi `/appunti 3D`
**Security** → S1 LAB: lezione pronta, eseguire le 6 sezioni su VM Kali → poi `/appunti S1`

---

## Scadenze Esami

| Esame | Data | Ora |
|-------|------|-----|
| Diritto dell'Informatica T | **16/06/2026** | 09:30 |
| Lab Amministrazione di Sistemi T | **22/06/2026** | 09:00 |
| Lab Sicurezza Informatica T | **17/07/2026** | 14:00 |

Piano fasi e stime ore dettagliate: `ESAMI SCELTI.md`
