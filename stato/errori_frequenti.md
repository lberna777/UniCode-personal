# Errori Frequenti — Pattern Ricorrenti

> Aggiornato automaticamente da `/appunti` quando vengono corretti bug o imprecisioni.
> Letto da `/ripassa` e `/simula` per generare domande mirate sui punti deboli.
> Letto da `/lezione` per enfatizzare concetti dove Lorenzo tende a sbagliare.

---

## SysAdmin — Bash / Linux

### Sintassi Bash
| Errore | Modulo | Correzione |
|--------|--------|------------|
| `[ !-d ]` senza spazio | 1B | `[ ! -d ]` — spazio obbligatorio tra `!` e operatore |
| Logica invertita in condizioni | 1A, 1B | Testare sempre con caso limite prima di fidarsi |
| `done` mancante nei loop | 1A | Ogni `for`/`while` deve avere il suo `done` |
| Shebang incompleto | 1A | Sempre `#!/bin/bash` come prima riga |

### Concetti Linux
| Errore | Modulo | Correzione |
|--------|--------|------------|
| Confusione contare righe vs occorrenze con grep | 0B, es_02 | `grep -c` = righe, `grep -o \| wc -l` = occorrenze |

---

## Diritto — Imprecisioni Giuridiche

### Terminologia
| Errore | Modulo | Correzione |
|--------|--------|------------|
| Regolamenti UE: detti "non direttamente applicabili" | D1 | Regolamenti UE sono direttamente applicabili per definizione |
| Direttive UE: dette "ideali" | D1 | Direttive sono vincolanti quanto al risultato, non "ideali" |
| Diritti morali = 70 anni | D3 | Diritti morali sono imprescrittibili; 70 anni = diritti patrimoniali |
| Forma espressiva = funzione del software | D3 | La tutela copre la forma espressiva, non la funzione |
| Dato sensibile = capacità identificativa | D8 | Dato sensibile = natura dell'informazione (salute, orientamento, ecc.), non capacità identificativa |
| CC BY = pubblico dominio | D5 | CC BY ≠ pubblico dominio; CC0 = rinuncia totale inclusa attribuzione |
| FEQ definita genericamente | D9 | FEQ = dispositivo qualificato + certificato qualificato (due elementi precisi) |
| "danno" usato al posto di "nocumento" | D11 | Nocumento ≠ danno generico: è pregiudizio giuridicamente rilevante (condizione oggettiva di punibilità art. 621) |
| Titolo sezione parafrasato invece del nome del reato | D11 | Il reato si chiama "Intercettazione, impedimento o interruzione illecita" — non "Rivelazione di Intercettazioni" |

### Pattern Ricorrenti Diritto
- **Tendenza a semplificare le distinzioni**: Lorenzo fonde concetti che il PDF tiene separati (es. variazioni richieste vs necessarie in D6, doppia base art. 6 + art. 9 in D8)
- **Definizioni parafrasate invece di fedeli al PDF**: il PDF della professoressa usa formulazioni precise che vanno riprodotte, non riformulate
- ~~Articoli citati senza numero preciso~~ → **NON rilevante**: la prof. ha confermato che numeri di articoli/leggi/date NON vanno memorizzati per l'esame (slide InfoGenerali, p. 8)

---

## Come Aggiornare

Quando `/appunti` identifica un bug o un'imprecisione:
1. Verificare se il pattern esiste già in questo file
2. Se sì: incrementare il contatore o aggiungere il nuovo modulo alla riga esistente
3. Se no: aggiungere una nuova riga nella sezione appropriata
4. Se emerge un pattern ricorrente (stesso tipo di errore in 3+ moduli): aggiungerlo alla sezione "Pattern Ricorrenti"
