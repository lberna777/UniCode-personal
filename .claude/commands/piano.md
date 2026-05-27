---
description: "Genera il piano di studio per oggi basandosi sullo stato, le scadenze e la fase corrente."
---

Leggi in parallelo:
- `stato/corrente.md`
- `ESAMI SCELTI.md`
- `stato/tracker_ripasso.md`

La data di oggi è disponibile nel contesto. Calcola i giorni mancanti a ciascun esame:
- Diritto: 16/06/2026
- SysAdmin: 22/06/2026
- Security: 17/07/2026

Determina la fase corrente del piano settimanale e identifica il prossimo modulo per ciascuna materia.

Produci esclusivamente:

---

**Piano di oggi — [DATA]**

**Scadenze**: Diritto tra X gg (16/06) · SysAdmin tra X gg (22/06) · Security tra X gg (17/07)

**Fase corrente**: [descrizione fase]

---

**Blocco 1 — [Materia] · ~Xh**
[Modulo ID] — [azione concreta: cosa fare, quale esercizio, quale file]

**Blocco 2 — [Materia] · ~Xh**
[Modulo ID] — [azione concreta]

**Blocco 3 — [Materia] · ~Xh**
[Modulo ID] — [azione concreta]

---

**Segnali di rischio** (solo se presenti):
- Moduli in ritardo rispetto alla fase
- Materie con troppi moduli aperti rispetto alla scadenza
- A questo ritmo: [stima se ci si arriva o no, basata su moduli rimasti / giorni rimasti / ore per modulo da ESAMI SCELTI.md]

**Ripasso consigliato** (solo se presente):
- [moduli con ripasso scaduto da tracker_ripasso.md — suggerire 15-20 min a inizio giornata]

---

Regole:
- I tre blocchi seguono l'allocazione oraria della fase corrente
- La materia più a rischio rispetto alla scadenza va nel Blocco 1
- Se un modulo ha lezione pronta ma pratica non fatta, segnalarlo
- Se per Security manca il PDF: blocco = "Richiedere PDF da Virtuale"
- Non aggiungere testo libero
