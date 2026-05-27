---
description: "Crea la lezione strutturata per un modulo dai PDF Virtuale. Uso: /lezione <ID>  (es. /lezione 3A, /lezione D1, /lezione S4)"
argument-hint: "ID modulo — SysAdmin: 0A-3F | Security: S1-S12 | Diritto: D1-D13"
---

Il modulo richiesto è: $ARGUMENTS

**Rileva il tipo di modulo dal prefisso dell'ID:**
- ID inizia con `D` → modulo **Diritto** (teoria, nessuna VM)
- ID inizia con `S` → modulo **Security** (lab Kali Linux)
- ID inizia con cifra → modulo **SysAdmin** (lab Vagrant/Debian)
- ID vuoto o non riconosciuto → mostra i formati validi e fermati

---

**1. Carica il contesto necessario**

Leggi questi file in parallelo:
- `stato/corrente.md` — verifica che il modulo esista e il suo stato attuale
- `stato/percorso.md` — recupera: nome completo, corso, materiale Virtuale richiesto, concetti chiave, esercizio attivo, connessioni
- `stato/errori_frequenti.md` — identifica pattern di errore ricorrenti di Lorenzo rilevanti per questo modulo (es. se sta facendo un modulo bash e ha pattern di errori di sintassi, enfatizzare quei punti)

Se il modulo non esiste nel percorso, comunicalo e fermati.

---

**2. Verifica i PDF**

Cerca i PDF in base al tipo di modulo:
- SysAdmin: `SLIDE TEORIA/SYSADM/` e `SLIDE LAB/SYSADM/`
- Security: `SLIDE TEORIA/SICINF/` e `SLIDE LAB/` (se esistono)
- Diritto: `SLIDE TEORIA/DIRITTO INFORMATICO/`

Se uno o più PDF richiesti mancano: **fermati**, elenca i nomi esatti da caricare e chiedi a Lorenzo. Non creare contenuto senza il PDF corrispondente.

---

**3. Leggi i PDF**

Leggi integralmente tutti i PDF rilevanti. Per PDF molto lunghi (>50 pagine), leggi per sezioni e identifica le parti pertinenti al modulo.

> **REGOLA CRITICA**: il contenuto della lezione deve venire SOLO dai PDF letti in questo passo. I "concetti chiave" in percorso.md sono un indice per sapere quali PDF cercare — NON sono una fonte da cui generare contenuto. Se non hai letto il PDF, non puoi creare la lezione. Contenuto generato senza leggere il PDF è superficiale e inaccettabile.

---

**4. Crea il file lezione**

Path: `/home/lorenzo/UniCode/claudeLezioni/<SOTTOCARTELLA>/lezione_modulo$ARGUMENTS_<nome_breve>.md`

Sottocartelle:
- SysAdmin → `LEZIONI SYSADM/`
- Security → `LEZIONI SECURITY/`
- Diritto → `LEZIONI DIRITTO/`

`<nome_breve>` = identificatore conciso del contenuto (es. `systemd_servizi`, `diritto_autore`).

---

### Template SysAdmin (ID numerico)

```
# Lezione — Modulo $ARGUMENTS: <Nome Completo>
**Corso**: Lab Amministrazione di Sistemi T
**Materiale**: <titoli PDF usati>
**Prerequisiti**: <moduli precedenti rilevanti — verificare che siano ✅ in corrente.md>

---

## Obiettivo
Una frase: cosa Lorenzo deve saper fare sulla VM al termine.

## Concetti Chiave
Per ogni concetto:
- **Definizione**: cos'è
- **Perché esiste**: quale problema risolve
- **Come si usa**: sintassi e contesto pratico su Debian

## Comandi di Riferimento
| Comando | Sintassi | Descrizione | Output atteso |
|---------|----------|-------------|---------------|

## Esercizi Guidati
Sequenza numerata di comandi da eseguire sulla VM.
- Ogni comando significativo ha l'output atteso
- Progressione: facile → difficile
- Se Lorenzo ha errori ricorrenti su concetti in questo modulo (da errori_frequenti.md): aggiungere un esercizio specifico che forza la comprensione corretta

## Connessioni
- Con il modulo precedente: [connessione SPECIFICA, non generica]
- Con Security: [quale superficie d'attacco introduce — essere precisi]

## Riepilogo
3 concetti chiave in forma di domanda-risposta (non lista passiva)
```

---

### Template Security (prefisso S)

```
# Lezione — Modulo $ARGUMENTS: <Nome Completo>
**Corso**: Lab Sicurezza Informatica T
**Materiale**: <titoli PDF usati>
**Prerequisiti**: <moduli SysAdmin e Security rilevanti — verificare che siano ✅>

---

## Obiettivo
Una frase: cosa Lorenzo deve saper fare/riconoscere al termine.

## Contesto e Threat Model
- **Prospettiva attaccante**: perché questo attacco funziona, cosa cerca
- **Prospettiva difensore**: come si rileva, come si mitiga
- Scenario reale documentato (se presente nel PDF)

## Concetti Chiave
Per ogni concetto: definizione tecnica, come si manifesta, esempio reale.

## Tool e Comandi
| Tool | Comando | Scopo | Output tipico |
|------|---------|-------|---------------|

## Esercizi Guidati
Sequenza su Kali Linux.
> ⚠️ Esegui uno snapshot della VM prima di iniziare.

## Connessioni
- Con SysAdmin: [quale configurazione errata viene sfruttata — SPECIFICO]
- Con moduli Security precedenti/successivi: [catena logica]

## Riepilogo
3 concetti in forma domanda-risposta
```

---

### Template Diritto (prefisso D)

> **Regola vincolante**: l'esame verte sugli argomenti e spiegazioni del PDF della professoressa. Le definizioni devono rispecchiare il linguaggio del PDF — non riformulare, non parafrasare, non integrare con fonti esterne. Segnalare con `[fonte: PDF]` ogni affermazione tratta dalle slide. Registro accademico-giuridico. Usare paragrafi discorsivi dove il PDF lo fa.

```
# Lezione — Modulo $ARGUMENTS: <Nome Completo>
**Corso**: Diritto dell'Informatica T
**Materiale**: <titolo PDF usato>
**Normative di riferimento**: <leggi e decreti citati nel PDF, con estremi completi>

---

## Obiettivo
Una frase: quale istituto giuridico Lorenzo deve saper spiegare, nelle parole della professoressa.

## Quadro Normativo
Norme di riferimento con estremi completi. Solo quelle presenti nel materiale.

## Concetti Chiave
Per ogni concetto:
- Definizione ripresa fedelmente dal PDF [fonte: PDF]
- Ratio legis se spiegata dalla professoressa
- Esempi usati nelle slide
- Se Lorenzo ha pattern di errore su questo tipo di concetto (da errori_frequenti.md): aggiungere nota esplicita "⚠️ Attenzione: in passato hai confuso X con Y"

## Riferimenti Normativi
| Articolo / Norma | Contenuto (come descritto nel PDF) | Rilevanza per il corso |
|------------------|------------------------------------|------------------------|

## Casi e Scenari
Situazioni concrete dalla professoressa. Se non presenti nel PDF, omettere.

## Domande di Autoverifica
Cinque domande aperte del tipo che la professoressa potrebbe fare all'esame.
Almeno una domanda deve testare le distinzioni che Lorenzo tende a fondere (pattern da errori_frequenti.md).
1. ...
2. ...
3. ...
4. ...
5. ...

## Riepilogo
Tre concetti normativi centrali, formulati come nel PDF.
```

---

**5. Verifica qualità (checklist interna)**

Prima di comunicare il risultato, verifica:
- [ ] Ogni concetto nel PDF è stato coperto nella lezione
- [ ] SysAdmin: ogni comando ha output atteso
- [ ] Diritto: ogni definizione usa la terminologia esatta del PDF
- [ ] Gli esercizi sono progressivi e hanno output atteso
- [ ] Le connessioni sono specifiche (citano moduli e concetti precisi)
- [ ] Pattern di errore di Lorenzo sono stati integrati come avvertimenti

Se una checklist non è soddisfatta, correggi prima di procedere.

---

**6. Aggiorna lo stato**

In `stato/corrente.md`: segna il modulo come 🔄 se era ⬜.

---

**7. Comunica il risultato**

- Path del file creato
- Per SysAdmin/Security: indica di avviare la VM e seguire gli esercizi guidati
- Per Diritto: indica di leggere la lezione e rispondere alle domande di autoverifica prima di scrivere gli appunti grezzi
- Se sono stati integrati avvertimenti da errori_frequenti.md, menzionarlo brevemente
