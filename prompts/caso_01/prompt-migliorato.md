# Prompt Migliorato - Caso 1

## Prompt Migliorato

```txt
Contesto: App didattica di gestione ticket costruita con React. La pagina lista ticket
(componente TicketList) mostra i ticket aperti in una lista. Quando non ci sono ticket
aperti, il componente non mostra nulla: nessun testo, nessuna immagine, nessuna indicazione
per l'utente. Questo è il caso "empty state".

Task: Analizza il componente TicketList e descrivi come aggiungere un empty state visibile
quando la lista dei ticket aperti è vuota.

L'empty state deve:
- comparire solo quando l'array dei ticket ha lunghezza zero
- mostrare un messaggio testuale chiaro (es. "Nessun ticket aperto")
- non alterare il comportamento quando ci sono ticket presenti

Confini:
- Non scrivere codice, non produrre una patch, non aprire una PR
- Non toccare routing, filtri, pagina di dettaglio o altri componenti
- Non aggiungere feature (ordinamento, ricerca, paginazione)
- Limita l'analisi al solo componente che gestisce la lista

Output atteso: Un piano testuale in 4 punti che indica:
1. Il file o componente da modificare
2. La condizione da controllare (quando la lista è vuota)
3. Il messaggio da mostrare
4. Come verificare che l'empty state sia visibile a lista vuota e assente a lista piena

Verifica: La proposta è accettabile se, dopo l'intervento descritto, un utente con lista
vuota vede un messaggio chiaro al posto di una pagina bianca.

Prima di rispondere: elenca le assunzioni che stai facendo sul progetto, il criterio con
cui hai scelto la soluzione e come proponi di verificarla.
```

---

## Controllo Qualita'

| Criterio | Risposta |
| --- | --- |
| Contesto presente | Si - app React didattica, componente TicketList, scenario empty state |
| Confini espliciti | Si - no codice, no patch, no PR, no routing, no filtri, no nuove feature |
| Output atteso | Si - piano testuale in 4 punti numerati |
| Prova di controllo | Si - empty state visibile a lista vuota, assente a lista piena |
| Cosa chiede all'AI di non fare | No codice, no patch, no PR, non uscire dal componente lista |
| Esempi necessari e proporzionati | Zero-shot: nessun esempio, il pattern è descrivibile a parole |
| Evita chain-of-thought estesa | Si - chiede assunzioni, criterio e verifica, non una spiegazione lunga |

- È più specifico perché nomina lo scenario (empty state), il componente (TicketList),
  la condizione (array.length === 0) e il messaggio atteso
- Limita meglio il lavoro perché esclude esplicitamente routing, filtri, feature aggiuntive
  e produzione di codice
- Produce un output più verificabile perché definisce un criterio di accettazione binario
  (messaggio visibile vs. pagina bianca) e chiede un piano in 4 punti controllabili
- Lo classificherei come Controllabile
