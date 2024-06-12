# Proiect de Management al Procesului de Intervievare
Acest repository centralizează sub-module pentru un sistem complex de management al procesului de intervievare în cadrul unei companii IT. Fiecare sub-modul reprezintă o componentă microserviciu a aplicației web full-stack.

# Sub-module incluse:
 - Proiectul de Frontend: https://github.com/SerbanTiurbe21/interview-management-app-licenta
 - Microserviciul ce Gestionează Utilizatorii și Autentificarea: https://github.com/SerbanTiurbe21/user-keycloak
 - Microserviciul "Candidates": https://github.com/SerbanTiurbe21/CandidateMicroservice
 - Microserviciul de Topicuri și Întrebări: https://github.com/SerbanTiurbe21/questions-microservice
 - Microserviciul ce Gestionează Documentele de Feedback și Scor:
 - Serviciul de Gateway: https://github.com/SerbanTiurbe21/isds
 - Serviciul de Înregistrare Eureka: https://github.com/SerbanTiurbe21/EurekaService

# Cum să folosiți acest repository
Pentru a utiliza acest repository, urmați pașii de mai jos:

## Clonare repository
Clonați acest repository pe mașina locală folosind:

`git clone --recurse-submodules https://github.com/SerbanTiurbe21/TiurbeSerban-LucrareLicenta-UPT-AC-CTI.git`

## Actualizare sub-module
Dacă sub-modulele au fost actualizate, rulați următoarea comandă pentru a vă asigura că aveți cele mai recente versiuni:

`git submodule update --recursive --remote`

## Construire și Rulare
Fiecare sub-modul are propriile sale instrucțiuni de construire și rulare, specificate în fișierele README ale acestora. Navigați în directorul fiecărui sub-modul și urmați instrucțiunile.
