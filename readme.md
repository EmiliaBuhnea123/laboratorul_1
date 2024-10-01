# Laboratorul_1

## __Sarcina nr. 1. Analiza cererilor HTTP__

### _Date greșite_

### 1. Ce metodă HTTP a fost utilizată pentru a trimite cererea?

Pentru a trimite cererea a fost utilizată metoda HTTP - POST

### 2. Ce anteturi au fost trimise în cerere?

accept: \*/\*

accept-encoding: gzip, deflate

accept-language: en-US,en;q=0.9

connection: keep-alive

content-length: 36

content-type: application/x-www-form-urlencoded; charset=UTF-8

host: sandbox.usm.md

origin: http://sandbox.usm.md

referer: http://sandbox.usm.md/login/

user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/53 36 (KHTML, like Gecko) Chrome/128.0.0.0 Safari/537.36

x-requested-with: XMLHttpRequest

### 3. Ce parametri au fost trimiși în cerere?

username: student

password: studetpass

### 4. Ce cod de stare a fost returnat de server?

A fost returnat codul de stare 401 Unauthorized.

### 5. Ce anteturi au fost trimise în răspuns?

connection: keep-alive

content-type: text/plain;charset=UTF-8

date: Thu, 12 Sep 2024 08:50:50 GMT

server: nginx/1.24.0 (Ubuntu)

transfer-encoding:chunked

### _Date corecte_

### 1. Ce metodă HTTP a fost utilizată pentru a trimite cererea?

Pentru a trimite cererea a fost utilizată metoda HTTP - POST

### 2. Ce anteturi au fost trimise în cerere?

accept: \*/\*

accept-encoding: gzip, deflate

accept-language: en-US,en;q=0.9

connection: keep-alive

content-length: 32

content-type: application/x-www-form-urlencoded; charset=UTF-8

host: sandbox.usm.md

origin: http://sandbox.usm.md

referer: http://sandbox.usm.md/login/

user-agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/53 36 (KHTML, like Gecko) Chrome/128.0.0.0 Safari/537.36

x-requested-with: XMLHttpRequest

### 3. Ce parametri au fost trimiși în cerere?

username: admin

password: password

### 4. Ce cod de stare a fost returnat de server?

A fost returnat codul de stare 200 OK.

### 5. Ce anteturi au fost trimise în răspuns?

connection: keep-alive

content-type: text/plain;charset=UTF-8

date: Thu, 12 Sep 2024 09:18:52 GMT

server: nginx/1.24.0 (Ubuntu)

transfer-encoding:chunked

## __Sarcina nr. 2. Crearea cererilor HTTP__

### 1. Scrieți o cerere de tip GET către server la adresa http://sandbox.com, indicând în antetul User-Agent numele și prenumele dvs.

GET / HTTP/1.1

Host: sandbox.com

User-Agent: Buhnea Emilia

### 2. Scrieți o cerere de tip POST către server la adresa http://sandbox.com/cars, indicând în corpul cererii următorii parametri:
- make: Toyota
- model: Corolla
- year: 2020

POST /cars HTTP/1.1

Host: sandbox.com

Content-type: application/x-www-form-urlencoded; charset=UTF-8

make=Toyota&model=Corolla&year=2020

### 3. Scrieți o cerere de tip PUT către server la adresa http://sandbox.com/cars/1, indicând în antetul User-Agent numele și prenumele dvs., în antetul Content-Type valoarea application/json, iar în corpul cererii următorii parametri: json { "make": "Toyota", "model": "Corolla", "year": 2021 }

PUT /cars/1 HTTP/1.1

Host: sandbox.com

Content-type: application/json

User-Agent: Buhnea Emilia

```json
 {
    "make": "Toyota"
    "model": "Corolla"
    "year": "2021"
 }
```

### 4. Scrieți unul dintre posibilele răspunsuri ale serverului la cererea anterioară. http POST /cars HTTP/1.1 Host: sandbox.com Content-Type: application/json User-Agent: John Doe model=Corolla&make=Toyota&year=2020 Presupuneți situațiile în care serverul poate returna codurile de stare HTTP 200, 201, 400, 401, 403, 404, 500.

Request URL: http://sandbox.com/cars

Request Method: POST

Status Code: 201 Created 

Connection: keep-alive

Content-type: application/json

User-Agent: John Doe

```json
{
    "id": 1,
    "model": "Corolla",
    "make": "Toyota",
    "year": 2020
}
```

_200 OK - Serverul va returna acest cod dacă crerea a fost procesată cu succes, dar resursa deja există și nu se mai creează alta nouă._

_201 Created - Serverul va returna acest cod dacă cererea a fost procesată cu succes și a fost creată o nouă mașină._

_400 Bad Request- Serverul va returna acest cod dacă datele trimise în cerere sunt incorecte sau nu sunt valide._

_401 Unauthorized - Serverul va returna acest cod dacă utilizatorul nu este autentificat și nu are permisiunea de a crea o mașină._

_403 Forbidden - Serverul va returna acest cod dacă utilizatorul este autentificat, dar nu are permisiunea necesară pentru a crea o mașină._

_404 Not Found - Serverul va returna acest cod dacă resursa (http://sandbox.com/cars) nu a fost găsit pe server._

_500 Internal Server Error - Serverul va returna acest cod dacă acesta a întâmpinat o eroare internă neașteptată care a împiedicat finalizarea cererii._


### 5. Scrieți o cerere de tip DELETE la alegerea dvs. și să explicați de ce, în acest caz, este potrivit să utilizați metoda DELETE.

DELETE /cars/1 HTTP/1.1

Host: sandbox.com

Connection: keep-alive

User-Agent: Buhnea Emilia

_Metoda DELETE este potrivită, deoarece aceasta este metoda reposnsabilă de ștergerea unei resurse specifice de pe server și anume în acest caz resursa care are ID-ul 1. Acest ID este scris în URL._


# __Sarcina nr. 3. Sarcina suplimentară. HTTP_Quest__

Cuvântul secret - __OSMcAggoDTc5DwAdCERGe0FCV2dTSH5Q__


