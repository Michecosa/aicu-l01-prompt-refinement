# LLM Observation - Caso 1

## Prompt Testato

```txt
Contesto: App didattica di gestione ticket costruita con React. La pagina lista ticket (componente TicketList) mostra i ticket aperti in una lista. Quando non ci sono ticket aperti, il componente non mostra nulla: nessun testo, nessuna immagine, nessuna indicazione per l'utente. Questo è il caso "empty state".

Task: Analizza il componente TicketList e descrivi come aggiungere un empty state visibile quando la lista dei ticket aperti è vuota.

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

Verifica: La proposta è accettabile se, dopo l'intervento descritto, un utente con lista vuota vede un messaggio chiaro al posto di una pagina bianca.

Prima di rispondere: elenca le assunzioni che stai facendo sul progetto, il criterio con cui hai scelto la soluzione e come proponi di verificarla.
```

## Cosa Ha Assunto Il Modello

- Assunzione 1: Il componente si chiama `TicketList` e riceve l'array di ticket come prop (es. `tickets`)
- Assunzione 2: Lo stack è React puro senza librerie UI estern (niente Bootstrap, Tailwind, ecc.)
- Assunzione 3: L'empty state va inserito con una condizione ternaria o un early return dentro il render del componente, non come componente separato

## Cosa Mancava Nel Contesto

- Il nome reale del file e il percorso nel repo (es. `src/components/TicketList.jsx`)
- La struttura dell'array ticket
- Il sistema di stile in uso

## Nota Finale

Con il prompt originale il modello avrebbe potuto riscrivere il componente, aggiungere filtri, proporre test...
Con il prompt migliorato, il contesto esplicito (empty state, TicketList, array vuoto) ha orientato la risposta verso un piano preciso e limitato. I vincoli negativi (es. "Non aggiungere feature") funzionano meglio se accompagnati da un output atteso