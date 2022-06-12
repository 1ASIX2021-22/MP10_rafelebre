# INSTAL·LACICIÓ DEL SISTEMA GESTOR DE BASE DE DADES. (MySQL)

Primer que tot instal·larem el MySQL amb la comanda següent de la imatge.

![Selecció_001](https://user-images.githubusercontent.com/72452088/173246479-5413b361-b439-43b1-90f1-77d215f7393e.png)

Per entrar al mysql escriurem la comanda **mysql** pero ens dona error ja que amb l'usuari que accedim no podem entrar

![Selecció_002](https://user-images.githubusercontent.com/72452088/173246596-739521d5-cf71-47b3-a83c-b1c2e0074888.png)


Desrpés instal·larem el nmap amb la mateixa comanda que hem fet al mysql pero amb nmap

![Selecció_003](https://user-images.githubusercontent.com/72452088/173246642-3dda62f7-9dfa-4eac-a462-66cd2483d858.png)

Quan haurem instal·lat el nmap, posarem la comanda **nmap localhost** i mirarem el port del mysql i es el 3306

![Selecció_004](https://user-images.githubusercontent.com/72452088/173246728-a51abedd-2210-47ef-9d73-29e922f302bd.png)

Abans per accedir al mysql ens donava error per l'usuari , per solucionar aixo el que farem sera veure el docuymte /etc/mysql/debian.cnf, i com es pot veure a la imatge podem veure l'usuari i tambçe la seva contrasenya

![Selecció_005](https://user-images.githubusercontent.com/72452088/173246875-257b5c69-40fe-4bc1-b690-2646f462dc2f.png)

Com ja tenima la contrasenya i el usuari entrarem al mysql posan els parametres -p -u que son  el de usuari i la contrasenya. I el que farem sera posar la contrasenya que hem troobat el document i a la comanda posarem l'usuari també.

![Selecció_006](https://user-images.githubusercontent.com/72452088/173246953-bff03685-b472-475d-bbc0-7f497cd90f14.png)

Per veure les base de dades que tenim executarem la comanda **SHOW DATABSES;** i com es pot veure tenim unes base de dades creades pero son del sistema

![Selecció_007](https://user-images.githubusercontent.com/72452088/173247045-c45fc77e-6611-4597-a6a8-7b5a8dc370d5.png)

Seguidament crearem una base de dades que li direm tasks i ho farem amb la comanda **CREATE DATABASE tasks;** i si volem veuire les base de dades posarem la mateixa comanda que abans

![Selecció_008](https://user-images.githubusercontent.com/72452088/173247121-caa90222-8fd5-4045-ac59-0c5c85c8a0f3.png)

![Selecció_010](https://user-images.githubusercontent.com/72452088/173247124-d3521488-eff5-4354-b489-e7b253433e10.png)

Abans hem creat una base de dades i ara el que farem sera crear una taula amb descripcio text, completed boolen. I mirarem si hem creat be la taula dins de la base de dades

![Selecció_011](https://user-images.githubusercontent.com/72452088/173247210-115270ce-fcaf-43d9-a92b-b10f04c7e5ca.png)
![Selecció_012](https://user-images.githubusercontent.com/72452088/173247216-b93d7a0f-4d57-404e-9504-21e9a417be56.png)

Ara descarregarem l'arxiu del paquet de mysql i per aixo haurem d'anar a la pagina i descarregarem el de 64 bits, anirem al directoriu de baixades i com podem veure si que tenim el paquet descarregat correctament

![Selecció_013](https://user-images.githubusercontent.com/72452088/173247282-03892d89-e392-4c43-9bd7-88a293478392.png)

![Selecció_014](https://user-images.githubusercontent.com/72452088/173247287-f1201e21-4f98-4fcb-b31c-eb12b88f1d0e.png)

Instal·larem el paquet amb el **dpkg -i**

![Selecció_016](https://user-images.githubusercontent.com/72452088/173247419-45041eca-75bd-422c-9e9e-1b5d8baea2af.png)

Com podem veure a la imatge ens dona error, per a solucionar aquest error ho farem amb la comanda **apt install mysql-workbench-community**

![Selecció_017](https://user-images.githubusercontent.com/72452088/173247423-f1c37d84-5b88-4b5f-aa92-3fb29febaf13.png)

I com ens demana fer apt --fix-broken install que per arreglar la instl·lació, ho farem 

![Selecció_018](https://user-images.githubusercontent.com/72452088/173247449-493e0e3c-47e0-4bec-b460-daceed37ca01.png)

Per finalitzar totes les instal·lacions de mysql, el que haurem de fer sera els ultims paquets que ens queden
![Selecció_019](https://user-images.githubusercontent.com/72452088/173247477-38c67ec9-c9c7-49aa-a89a-18f861ff8e7a.png)

Com ja ho tenim tot instal·lat, obrirem el work bench amb la comanda de la imatge

![Selecció_020](https://user-images.githubusercontent.com/72452088/173247505-1cd3a7af-5ff1-4ad4-b291-dd01421c4aa3.png)
![Selecció_021](https://user-images.githubusercontent.com/72452088/173247507-d9eb2c67-e879-40cc-8452-4a4c3c846395.png)

Pèr conectarnos a la nostra instancia local, el que haurem de fer es corregir el usuari d'inici de sessió i la contrasenya, que seran els mateixos que hem vist al arxiu d'abans i com es pot veure ja tenim la conexio completada al nostre mysql
![Selecció_022](https://user-images.githubusercontent.com/72452088/173247583-de8d1682-90c9-4ec5-aa8e-62ddbd83f8aa.png)
![Selecció_023](https://user-images.githubusercontent.com/72452088/173247599-8bf67645-a18a-4351-a569-ef091bd827d2.png)

I com podem veure a la imatge, com que ja tenim la conexio feta cap al nostre mysql, ja podem veure tot el que hem creat abans que es la taula de tasks
![Selecció_024](https://user-images.githubusercontent.com/72452088/173247633-a5cb4316-7c30-4b1d-928e-28be2efd1a82.png)

Amb el meu cas ja tinc el PHPSTORM instal·lat, lñ'unic que haure de fer es obrir-lo i crear un projecte buit

![Selecció_025](https://user-images.githubusercontent.com/72452088/173247666-d9dcb1bc-98ef-436f-9824-ea56d7c06fa7.png)

Quan estem dins del projecte que hem creat, ens apareixera un missatge que ens diu que falten paquets de drivers, per solucionar aquest error el que farem sera instal·lar el paquet que fa falta que esl el **php7.4-mysql**

![Selecció_027](https://user-images.githubusercontent.com/72452088/173248266-a3a0695f-f756-4801-9f37-b665e1ebb8ad.png)

Una vegada instal·lem els paquets necessaris ja podrem iniciar sessio amb les mateixes credeencials que abans
![Selecció_028](https://user-images.githubusercontent.com/72452088/173248294-d2bd6d36-6293-4fb3-95fa-ae91585cad17.png)

