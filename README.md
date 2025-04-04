# Proiect de Management al Procesului de Intervievare
Acest repository centralizează sub-module pentru un sistem complex de management al procesului de intervievare în cadrul unei companii IT. Fiecare sub-modul reprezintă o componentă microserviciu a aplicației web full-stack.

Fiecare sub-modul are un fișier de tip `read-me` propriu ce conține informații specifice fiecărui microserviciu/serviciu și poate fi accesat folosind link-urile din secțiunea de mai jos.

# Sub-module incluse:
 - Proiectul de Frontend: https://github.com/SerbanTiurbe21/interview-management-app-licenta
 - Microserviciul ce Gestionează Utilizatorii și Autentificarea: https://github.com/SerbanTiurbe21/user-keycloak
 - Microserviciul "Candidates": https://github.com/SerbanTiurbe21/CandidateMicroservice
 - Microserviciul de Topicuri și Întrebări: https://github.com/SerbanTiurbe21/questions-microservice
 - Microserviciul ce Gestionează Documentele de Feedback și Scor: https://github.com/SerbanTiurbe21/isds
 - Serviciul de Gateway: https://github.com/SerbanTiurbe21/GatewayService
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

Pentru proiectele care reprezintă partea de back-end va trebui să urmați toți pașii până înainte de `Rularea Containerului Docker` și să vă opriți aici pentru că astfel nu se va putea realiza pasul următor din acest readme.

## Rularea Tuturor Serviciilor Utilizând Docker Compose

După ce ați clonat repository-ul și ați actualizat sub-modulele, puteți utiliza Docker Compose pentru a construi și rula toate serviciile asociate proiectului într-un mod coordonat. În acest sens am pus la dispoziție un fișier docker-compose.yml pentru a rula toate containerele necesare funcționării corecte a backend-ului.

### Verificare și Instalare Docker Compose

Asigurați-vă că aveți Docker și Docker Compose instalate pe sistemul dvs. Acestea sunt necesare pentru a rula comenzi de Docker Compose. Docker Compose este inclus în majoritatea instalațiilor Docker pentru sistemele de operare Windows și Mac. Pentru Linux, s-ar putea să fie necesar să instalați Docker Compose separat.

Puteți verifica dacă Docker Compose este instalat și funcțional cu comanda:

`docker-compose --version`

### Rularea Serviciilor

Pentru a porni toate serviciile definite în fișierul `docker-compose.yml`, navigați în directorul rădăcină al proiectului unde se află acest fișier și rulați următoarea comandă:

`docker-compose up`

Aceasta va construi (dacă este necesar) și va porni toate containerele specificate pentru fiecare serviciu. Containerele vor fi legate conform configurărilor specificate, permițându-le să comunice între ele așa cum este definit în `docker-compose.yml`.

Dacă doriți să rulați serviciile în fundal, puteți folosi opțiunea `-d`:

`docker-compose up -d`

### Oprire și Curățare

Când doriți să opriți toate serviciile, puteți folosi comanda:

`docker-compose down`

Aceasta va opri toate containerele și va elimina containerele, rețelele create implicit, și volumul anonim, dar nu va șterge imagini construite.

Pentru o curățare completă, care include și ștergerea imaginilor construite, puteți folosi:

`docker-compose down --rmi all`
