# DIAGNOSI
```txt
Sistema la pagina dei ticket.
```

## Informazioni mancanti?
* Linguaggi di programmazione, frameworks o librerie da usare
* Componenti della pagina
* Struttura dati dei ticket 

## Ambiguità?
  * "Sistema" può significare correggere un bug, migliorare la UX, aggiungere una funzionalità o riscrivere un componente
  * "Pagina dei ticket" copre potenzialmente più componenti, rotte e stati (caricamento, errore, ecc.)
  * Non è chiaro se il problema riguarda un problema specifico o l'intera pagina

## Rischio di scope troppo largo?
  * L'AI potrebbe riscrivere l'intera pagina, aggiungere filtri, paginazione, routing o test
  * Nessun vincolo su cosa NON fare: tutto e' in gioco
  * Un prompt cosi' vago invita l'AI a inventare il contesto e allargare il lavoro

## Output non verificabile?
* Non c'è modo di verificare se l'output risolve il problema originario

## Bastano istruzioni Zero-shot o servono esempi Few-shot?
* L'IA ha bisogno di istruzioni few-shot per capire lo standard del codice e/o lo stile grafico da replicare


## Prompt Usato Per Migliorare

```txt
Aiutami a migliorare questo prompt.
Non risolvere il task.
Dimmi prima quali informazioni mancano.
Indica se basta una versione zero-shot o se servono 1-2 esempi few-shot.
Non mostrare chain-of-thought estesa: elenca solo assunzioni, criterio e verifica proposta.
Poi proponi una versione migliore.
```