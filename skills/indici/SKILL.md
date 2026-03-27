---
name: indici
description: >
  Usa questa skill ogni volta che Duccio vuole costruire un indice sintetico per valutare, 
  comparare o decidere su qualsiasi oggetto professionale: candidati, ruoli, opportunità, 
  report, clienti, offerte, progetti, percorsi di carriera, contesti organizzativi.
  
  Trigger tipici: "costruiamo un indice per...", "come valutiamo...", "dammi uno score per...", 
  "quanto è affidabile questo...", "conviene questo ruolo?", "che punteggio darei a...", 
  "mi fai un indice di...", "calcoliamo la convenienza di...", "indice di...".
  
  Usa questa skill anche proattivamente quando Duccio sta valutando un'opportunità, 
  un candidato, un report o una proposta e non ha ancora chiesto esplicitamente un indice — 
  se la situazione si presta, proponi di costruirne uno.
---

# Skill INDICI — Sistema di Valutazione Sintetica

## Scopo

Costruire e applicare indici sintetici per trasformare valutazioni qualitative complesse 
in numeri azionabili. Gli indici di Duccio hanno queste caratteristiche:
- Dimensioni pesate (ogni dimensione ha un peso che riflette la sua importanza strategica)
- Scale coerenti (di norma 1–5 per dimensione)
- Output con semaforo (🟢 verde / 🟡 giallo / 🔴 rosso)
- Soglie calibrate sul contesto specifico

---

## Libreria Indici Validati

### INDICE 1 — Affidabilità Report

**Oggetto:** Misura quanto sono attendibili le informazioni contenute in un report 
(profilazione candidato, assessment, reference check, scheda candidato, ecc.), 
basandosi sulla qualità delle fonti di ciascuna dimensione valutata.

**Formula:**
```
Affidabilità % = Σ(certezza_i) / N_dimensioni
```

**Livelli di certezza per dimensione:**
| Stato | Valore |
|-------|--------|
| Certo da CV / fonte diretta | 100% |
| Inferito da dati correlati | 60% |
| Stimato / estrapolato | 35% |

**Semaforo:**
| Score | Colore | Significato |
|-------|--------|-------------|
| ≥ 75% | 🟢 Verde | Alta affidabilità |
| 50–74% | 🟡 Giallo | Affidabilità parziale, segnalare al cliente |
| < 50% | 🔴 Rosso | Bassa affidabilità, integrare con altre fonti |

**Caso di riferimento — Claudia Chiti (83%):**
```
Dimensione               Stato        Valore
Brillantezza Studi       Certo        100%
Innovazione              Certo        100%
Dimensione Strategica    Inferito      60%
Stabilità                Certo        100%
Specializzazione         Certo        100%
Execution                Certo        100%
Internazionalità         Certo        100%
Mobilità                 Stimato       35%
Trasversalità            Certo        100%
Gestione Stakeholder     Inferito      60%
Progressione             Certo        100%
Dimensione Ruolo         Stimato       35%
─────────────────────────────────────────
Σ = 990 / 12 = 82.5% → 83% 🟢 Verde
```

---

### INDICE 2 — Opportunity Score (Convenienza Ruolo per Candidato)

**Oggetto:** Valuta se un'opportunità lavorativa è strategicamente conveniente 
per un candidato specifico, considerando fit, contesto, remunerazione, visibilità, 
reversibilità e effetto rete.

**Dimensioni e pesi:**
| # | Dimensione | Peso | Descrizione |
|---|-----------|------|-------------|
| 1 | Fit con obiettivo dichiarato | ×3 | L'opportunità avvicina o allontana dal goal strategico del candidato? |
| 2 | Qualità del contesto organizzativo | ×3 | Il capo diretto, la cultura, il modo in cui si premia chi lavora |
| 3 | Remunerazione adeguata | ×2 | Non solo il numero: coerenza contributo/compenso, equity, valore indiretto |
| 4 | Visibilità e personal brand | ×2 | Costruisce reputazione nel posizionamento target o è invisibile? |
| 5 | Reversibilità | ×1 | Se non funziona, quanto è facile uscire senza danni? |
| 6 | Effetto rete | ×1 | Apre porte rilevanti o è un binario morto? |

**Scala:** 1–5 per ogni dimensione  
**Score massimo:** (5×3) + (5×3) + (5×2) + (5×2) + (5×1) + (5×1) = **65 punti**

**Soglie:**
| Score | Semaforo | Indicazione |
|-------|----------|-------------|
| > 45 | 🟢 Verde | Vai, ha senso strategico |
| 35–45 | 🟡 Giallo | Valuta con attenzione, negozia le condizioni |
| < 35 | 🔴 Rosso | Rischio alto di distrazione |

---

## Metodo Generativo — Come Costruire un Nuovo Indice

Quando Duccio vuole un indice nuovo, seguire questi passaggi:

### Step 1 — Definire l'oggetto
> Cosa stiamo valutando? (candidato, ruolo, cliente, proposta, report, contesto...)

### Step 2 — Identificare le dimensioni
Chiedere a Duccio: "Quali sono i fattori che contano davvero per giudicare questo oggetto?"
- Di norma: 4–8 dimensioni (meno = troppo semplice, più = rumore)
- Ogni dimensione deve essere osservabile o valutabile concretamente

### Step 3 — Assegnare i pesi
- Peso ×3 → dimensioni critiche, discriminanti
- Peso ×2 → dimensioni importanti
- Peso ×1 → dimensioni secondarie ma rilevanti
- Alternativa: pesi uguali (come nell'Indice Affidabilità) se tutte le dimensioni hanno uguale importanza

### Step 4 — Scegliere la scala
- **Scala 1–5** (standard): adatta per giudizi qualitativi
- **Scala percentuale** (0–100%): adatta per dati quantitativi o binari
- **Scala mista**: se alcune dimensioni sono quantitative e altre qualitative

### Step 5 — Calcolare lo score massimo
```
Score_max = Σ(scala_max × peso_i)
```

### Step 6 — Calibrare le soglie
Proporre soglie a Duccio basandosi su questa logica di default:
- 🟢 Verde: ≥ 70% dello score massimo
- 🟡 Giallo: 50–69% dello score massimo
- 🔴 Rosso: < 50% dello score massimo
Poi aggiustare insieme in base al contesto specifico.

### Step 7 — Applicare e verificare
Applicare l'indice a un caso concreto noto, verificare che il risultato 
sia intuitivamente corretto. Se non lo è, rivedere pesi o soglie.

---

## Regole di Stile

- Gli indici si presentano sempre in forma tabellare, con semaforo finale visibile
- Il nome dell'indice è in MAIUSCOLO e descrittivo (es. "OPPORTUNITY SCORE", non "indice 2")
- Quando si applica un indice a un caso reale, mostrare sempre il calcolo riga per riga
- Le soglie si esprimono sempre in termini assoluti (punti) E in percentuale sul massimo
- Quando si aggiunge un nuovo indice validato alla libreria, segnalarlo a Duccio 
  con: "Vuoi che aggiunga questo indice alla libreria della skill INDICI?"

---

## Espansione Futura

Ogni nuovo indice costruito e validato con Duccio va aggiunto alla sezione 
"Libreria Indici Validati" con:
1. Nome in MAIUSCOLO
2. Oggetto (una riga)
3. Dimensioni e pesi in tabella
4. Formula o metodo di calcolo
5. Soglie con semaforo
6. Caso di riferimento (se disponibile)
