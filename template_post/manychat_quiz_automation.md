# ManyChat — Automazione "Commenta QUIZ"
## Setup per il Quiz "Come sta il tuo corpo?"

---

## LOGICA DEL FLUSSO

```
Utente commenta "QUIZ" su un Reel
        ↓
ManyChat invia DM automatica (entro 30 sec)
        ↓
Utente clicca il link → completa il Quiz
        ↓
Arriva in Brevo segmentato per profilo (intestino / ormoni / mente)
        ↓
Email automatica per profilo → offerta Reset 7 (€47)
```

---

## CONFIGURAZIONE MANYCHAT

### Passo 1 — Crea il flow
1. Apri ManyChat → **Flows → New Flow**
2. Nome: `RINATA - Commenta QUIZ`
3. Trigger: **Instagram Comment → parola chiave "QUIZ"** (case insensitive)
4. Aggiungi anche varianti: "quiz", "Quiz", "QUIZ!" per catturare tutto

### Passo 2 — Messaggio DM automatico (IMMEDIATO)

> **Messaggio 1 — Inviato subito dopo il commento**

```
Ciao [Nome]! 👋

Ho visto che vuoi scoprire com'è messo davvero il tuo corpo.

Ho preparato un quiz veloce (3 minuti) che identifica se il tuo blocco principale è:
👉 Intestino
👉 Ormoni  
👉 Mente

In base al tuo profilo ti mando subito cosa fare.

Clicca qui → [LINK AL QUIZ]

A dopo,
Marisa
```

**Note di configurazione:**
- `[Nome]` = variabile ManyChat `{{first name}}`
- `[LINK AL QUIZ]` = URL del quiz su metodorinata.it con parametro UTM: `?utm_source=instagram&utm_medium=dm&utm_campaign=quiz-commento`
- Aggiungi pulsante cliccabile: **"Fai il quiz ora →"**

---

### Passo 3 — Follow-up (se non clicca entro 24h)

> **Messaggio 2 — Inviato 24 ore dopo SE non ha cliccato il link**

```
[Nome], volevo solo assicurarmi che avessi ricevuto il link 😊

Tante donne mi dicono che pensavano di sapere qual era il loro problema principale... e il quiz le ha sorprese.

Il quiz è gratuito e dura 3 minuti:
→ [LINK AL QUIZ]

Ci sono 3 profili completamente diversi — intestino, ormoni, mente — con percorsi diversi per ognuno.

Marisa
```

**Condizione:** invia solo se `link_clicked = false`

---

### Passo 4 — Messaggio di ringraziamento post-click (opzionale ma consigliato)

> **Messaggio 3 — Inviato quando clicca il link**

```
Perfetto! Tra qualche minuto ricevi i tuoi risultati via email 📩

Controlla anche la cartella spam se non li trovi subito.

Se hai domande scrivimi qui, rispondo personalmente.

Marisa 🌿
```

---

## SCRIPT CTA DA INSERIRE NEI REEL

### Regola base
La CTA va negli **ultimi 5 secondi** del Reel, a voce + testo sovrapposto.

---

### CTA TIPO A — Per Reel educational (fame, vampate, gonfiore)

**Visivo:** testo a schermo "Commenta QUIZ"  
**Audio di Marisa:**

> *"Se vuoi capire qual è il tuo blocco principale — se è l'intestino, gli ormoni o la mente — commenta qui sotto la parola QUIZ e ti mando subito il link in privato."*

---

### CTA TIPO B — Per Reel storia personale

**Visivo:** testo a schermo "Scrivi QUIZ nei commenti"  
**Audio di Marisa:**

> *"Anch'io ero ferma lì, finché non ho capito da dove ripartire. Se vuoi scoprire il tuo punto di partenza, scrivi QUIZ nei commenti — ti rispondo io personalmente."*

---

### CTA TIPO C — Per Reel trasformazione/risultato

**Visivo:** testo a schermo "Commenta QUIZ per il tuo profilo"  
**Audio di Marisa:**

> *"Questo risultato è possibile quando parti dal profilo giusto per te. Commenta QUIZ e ti dico subito da dove cominciare tu."*

---

### CTA per le STORIES (con link sticker)

Usa il link sticker direttamente all'URL del quiz.  
Testo sovrapposto: **"Scopri il tuo profilo RINATA →"**

Story sequence consigliata (3 slide):
1. Domanda: *"Sai qual è il vero blocco che ti frena?"*
2. I 3 profili: *"Intestino · Ormoni · Mente — quale sei tu?"*
3. CTA: link sticker + *"3 minuti e lo scopri gratis"*

---

## PARAMETRI UTM DA USARE

| Canale | UTM source | UTM medium | UTM campaign |
|--------|-----------|------------|-------------|
| DM ManyChat (commento) | instagram | dm | quiz-commento |
| Story link sticker | instagram | story | quiz-story |
| Link in bio | instagram | bio | quiz-bio |
| IG Live | instagram | live | quiz-live |

Aggiungili sempre all'URL del quiz per tracciare da dove arrivano le conversioni.

---

## OBIETTIVI E KPI

| KPI | Target settimanale |
|-----|-------------------|
| Commenti "QUIZ" ricevuti | 20+ |
| DM aperte / commenti | >70% |
| Click sul link / DM aperte | >40% |
| Quiz completati / click | >60% |
| Email acquisite / quiz completati | 100% (automatico) |

---

## NOTE TECNICHE

- **Piano ManyChat necessario:** Pro (per le automazioni Instagram)
- **Connessione richiesta:** Instagram Business + Facebook Page collegate a ManyChat
- **Link in bio aggiornato:** metodorinata.it/quiz (redirect a Linktree o diretto)
- **Brevo:** configurare la tag per ogni profilo (intestino / ormoni / mente) in base alla risposta del quiz — la segmentazione automatica è il cuore del funnel
