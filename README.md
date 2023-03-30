Milestone 3
nome repo 2: vite-boolfolio
Iniziamo ad occuparci della parte front-office della nostra applicazione: creiamo un nuovo progetto Vue 3 con Vite e installiamo axios.
Colleghiamo questo progetto ad una repo separata. OK

Milestone 4
Nel componente principale della nostra Vue App facciamo una chiamata API all'endpoint costruito nel progetto Laravel (milestone 1) e recuperiamo tutti i progetti dal nostro back-end.
Stampiamo in console i risultati e verifichiamo di ricevere i dati correttamente. OK

Milestone 5
Creiamo un nuovo componente ProjectCard, che corrisponde ad una card per visualizzare un progetto. Utilizziamo questo componente per visualizzare tutti i progetti ricevuti tramite API. OK


CONSEGNA 30-3
Aggiungiamo l'endpoint API projects/slug (corrispondente alla funzione show nel controller) per recuperare le informazioni del singolo Progetto tramite axios

Milestone 1
nome repo 1: laravel-api
Creiamo la funzionalità show in Api\ProjectController

Milestone 2
Testiamo la chiamata API tramite Postman e assicuriamoci di ricevere i dati correttamente

Milestone 3
nome repo 2: vite-boolfolio
Aggiungiamo Vue Router sul front office e creiamo almeno 2 rotte:
Rotta per l'index dei progetti
Rotta per lo show del singolo progetto

Milestone 4
Nella pagina del singolo progetto, recuperare le informazioni tramite API e mostrarle in pagina
