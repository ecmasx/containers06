## 1. Crearea unei aplicații multi-container

Scopul lucrării
Famialiarizarea cu gestiunea aplicației multi-container creat cu docker-compose.

### 1. Configurarea fișierului docker-compose.yml

Primul pas in crearea aplicatiei multi-container este configurarea fisierului docker-compose.yml. Acest fisier definește serviciile, rețelele și volumele necesare pentru aplicația noastră.

![Crearea fisierului docker-compose.yml](/images/docker%20compose%20yml.png)

### 2. Configurarea variabilelor de mediu pentru MySQL

Pentru a asigura securitatea si configurarea corecta a bazei de date, am creat fisierul mysql.env care contine variabilele de mediu necesare pentru containerul MySQL.

![Crearea fisierului mysql.env](/images/my_sql.png)

### 3. Pornirea containerelor

Dupa configurarea fisierelor necesare, am pornit containerele folosind comanda docker-compose up. Aceasta comanda creeaza si porneste toate serviciile definite in docker-compose.yml.

![Pornirea containerului](/images/docker%20compose%20up.png)

### 4. Verificarea rezultatului

Dupa pornirea containerelor, am verificat starea lor pentru a ne asigura ca toate serviciile functioneaza corect.

![Rezultatul](/images/rezultat.png)

### 5. Accesarea aplicației

In final, am accesat aplicatia prin browser la adresa localhost pentru a verifica functionalitatea completa a sistemului.

![Accesarea paginii web](/images/localhost.png)

Întrebări
Cum doua containere pot interactiona unul cu celalalt
Containerele pot interactiona intre ele printr-o conexiune locala sau folder comun.

Cum vedem containerele unul pe celalalt in cadrul retelei interne?
Dockerul tine cont de denumirile containerelor in retea in care sunt rulate. Ei pot accesa unul pe altul prin numele container-ului.

De ce a fost necesar să se suprascrie configurarea nginx?
Asta era necesar pentru ca php si nginx sa aiba acces comun la pagina web. Nginx ofera paginile statice, precum html, css si javascript, iar php proceseaza paginile dinamice.

Concluzie
In aceasta lucrare de laborator am rulat doua containere, unul pentru website, altul pentru pagini web, le-am legat prin-tro retea docker si am afisat o pagina in browser.
