---
layout: default
title: "Sprint 2: Gestió de la Informació del Sistema i Administració"
---

## Sistemes de fitxers i particions

- Mida del sector

Un sector es la unitat minima fisica on es guarden les dades al disc. Aquesta mida no la podem modificar

Per a trovar la mida del sector farem un fdisk -l

<img width="661" height="161" alt="imagen" src="https://github.com/user-attachments/assets/92e89ad9-04f7-4755-941e-f084a3edcd8d" />


- Mida del block

Un block es la unitat minima logica on es guarden les dades a nivell del sistema operatiu. Aquesta mida es de 4096 bytes on aquesta mida si que pot ser modificada al moment de formatejar la partició

Per a mirar la mida del block usarem la comanda que es mostra en la següent imatge

<img width="474" height="91" alt="imagen" src="https://github.com/user-attachments/assets/f0c9876c-4948-4556-b409-3cc11b9d232b" />



<img width="786" height="380" alt="imagen" src="https://github.com/user-attachments/assets/be2a615d-6803-4ba2-bfa1-1654a828f3f5" />


- Fragmentació interna

Es basicament l'espai desaprofitat en els block on sobra espai, on podem fer que l'espai dels blocks que es de 4096 bytes el podem reduir. Depenent el sistema de fitxer que tingui la particio podrem reduir fins cert espai o un altre

- Fragmentació externa

La fragmentacio externa es quan a mesura que es va treballant en el sistema operatiu els arxius no es van guardant en blocks continuos de memoria fent aixi que el rendiment baixe entre altres coses. 
En windows tenim el desfragmentador per a reduir i en linux el sistema de fitxers es tant bo que no fa falta una eina pero si tu vulgueses usar alguna si que hi han  

Comanda per a comprovar si necesites desfragmentar el disk:

<img width="803" height="492" alt="imagen" src="https://github.com/user-attachments/assets/f2d3d6ed-b56a-4dcf-b388-df7d6c983cce" />

Comanda per a desfragmentar el disk es la mateixa pero llevant la -c:

<img width="803" height="492" alt="imagen" src="https://github.com/user-attachments/assets/7afe2a12-3733-4304-ad3f-a6ed4e10573e" />


- Tipus de sistemes de fitxers

Hi han molts d'ell. Ele més coneguts ext4 fat32 i ntfs

Aquests fitxers son els que usen les particions per a guardar tant com el sistema operatiu i els fitxers del sistema

- Tipus de formateig

Alt nivell: No borrem el sistema operatiu si no estem borrant el sistema de fitxers, on es pot recuperar usant eines externes

Mig nivell: No borrem el sistema operatiu si no estem borrant el sistema de fitxers i mira si te un sector defectuos i tels marca, on es pot recuperar usant eines externes

Baix nivell: Directament et borra tot el sistema operatiu sense opcio de recuperacio

- Particions/volums

Una particio es una separació del disc a nivell fisic, mentres que un volum es una capa d'abstraccio que es posa damunt de les paticions.

<img width="263" height="392" alt="imagen" src="https://github.com/user-attachments/assets/6ab5a433-9c5e-4b4c-be0c-1fd4f33e0585" />


  - GPARTED

Primer que tot instalem la eina gparted desde terminal. GParted és un programa molt senzill i visual per gestionar particions de disc.

<img width="742" height="347" alt="imagen" src="https://github.com/user-attachments/assets/f8d2ac24-f372-4d18-b8e8-bd71c05f6b1c" />

Una vegada instalada el que farem sera iniciarla i una vegada dins podrem observar el contingut de la app

<img width="783" height="273" alt="imagen" src="https://github.com/user-attachments/assets/22007975-65ee-4b7b-92fa-5cd774777101" />

  - comandes

Primer que tot mirarem el com al disc que em afegit de 10 GB no tenim ninguna partició així que tocara crear una

<img width="729" height="112" alt="imagen" src="https://github.com/user-attachments/assets/c4f50407-dcec-4335-bf93-0e013a23d3b4" />

Aquí com es pot observar després de seleccionar el disc crearem una partició

<img width="735" height="441" alt="imagen" src="https://github.com/user-attachments/assets/f439395b-1fb2-42a2-920e-5c312e1bc629" />

I si tornem al menu anterior podrem observar el com si que tenim ja feta la partició

<img width="741" height="214" alt="imagen" src="https://github.com/user-attachments/assets/3ccad7df-d911-46bc-95e9-fb7c2f0508e3" />

Aquí el que farem será el crear un sistema de fitxers ext4 a la partició recent creada

<img width="721" height="272" alt="imagen" src="https://github.com/user-attachments/assets/07debe5c-df52-4fca-8c44-637eba412bc4" />

Següent mirem si s’ha aplicat

<img width="587" height="80" alt="imagen" src="https://github.com/user-attachments/assets/d6efc12b-29c7-4241-b004-4de77176cfb2" />

Ara el que farem sera el crear un directori i un arxiu els quals els posarem dins de la partició recent feta on com es pot observar surt com a lost+found on si reiniciem ja no ens apareixerà ja que no tenim montat l'accés a la partició

<img width="608" height="371" alt="imagen" src="https://github.com/user-attachments/assets/80413fa7-54cf-42b7-b582-af69451f23ab" />

On per a fer-ho anirem a l’arxiu en /e	tc/fstab i afegirem la ultima linea que es mostrar que el que fa es que es monte l’acces cada vegada que entrem al ubuntu

<img width="743" height="354" alt="imagen" src="https://github.com/user-attachments/assets/589e1ca0-48b0-4913-b06c-1a0880ea4320" />

I com es pot observar funciona

<img width="740" height="105" alt="imagen" src="https://github.com/user-attachments/assets/f396b665-4669-4512-a41c-a4a3ffaf75a3" />


## Còpies de seguretat i automització de tasques

1- Teoria còpies de seguretat Còpia completa: Es fa una còpia de tot el seleccionat, ens quedem fora de duptes però sont grans i lentes. Actualment les millors. Còpia diferencial: A partir de la còpia completa, es resguarda la diferencia del contingut, afegint-se a la completa. Són ràpides i petites, però depenen de la còpia completa. Còpia incremental: A partir de la còpia completa, també es resguarda la diferencia del contingut, però cada incremental es guarda a partir de l'anterior. Són més petites encara, però en cas de backup cal totes les incrementals acumulades.

2- Teoria comandes backups+ cp: Comanda bàsica de copiar, utilitzada en entorns locals. No és intel·ligent. rsync: Crea sincronitzacions de carpetes, permet fer còpies en local i remot via SSH. És intel·ligent. dd: "dd" no és per a fer còpies, és per a clonar particions o discos. No és intel·ligent.

3- Pràctica comandes backup cp:

<img width="821" height="414" alt="imagen" src="https://github.com/user-attachments/assets/226d8764-df65-4f55-a26c-d8cf5c5b1aef" />

rsync:

<img width="821" height="414" alt="imagen" src="https://github.com/user-attachments/assets/76dbb61c-57be-42cc-b776-cd7bf84768db" />

dd: 

El comandament dd copia blocs de dades sense tenir en compte el sistema de fitxers. Per tant, el dispositiu destí ha de tenir una capacitat igual o superior a l’origen; en cas contrari, la còpia falla amb un error d’espai insuficient

<img width="727" height="383" alt="imagen" src="https://github.com/user-attachments/assets/0ed5b939-ea84-4c4a-8946-ca49db06ef5c" />



## Gestió d'usuaris, grups i permisos

En el fitxer passwd estan tots els usuaris del sistema

<img width="734" height="444" alt="image" src="https://github.com/user-attachments/assets/1bd4aa7b-7242-49aa-ade7-50ce1de09060" />

En el fitxer group estan tots els grups del sistema

<img width="734" height="444" alt="image" src="https://github.com/user-attachments/assets/4095a98e-c217-443e-ab02-733655b5ec06" />

En el fitxer shadow trovarem totes les contrasenyes encriptades junt a la seva data de caducitat

<img width="734" height="444" alt="image" src="https://github.com/user-attachments/assets/a5f63145-6137-4ca7-8c83-fa2247eac5ec" />

Al fitxer gshadow es veuen els administrador de cada grup

<img width="734" height="444" alt="image" src="https://github.com/user-attachments/assets/a2dec8b4-f3bd-473d-b91f-10c5a76da1dc" />

Per a crear un usuari usem adduser i el nom de l'usuari que volem crear 

<img width="722" height="343" alt="image" src="https://github.com/user-attachments/assets/c9001a8b-b850-4c3c-8a3f-479c81c0be42" />

Fins que no inicem sessio amb l'usuari de forma grafica no es crearan les carpetes corresponents

<img width="736" height="70" alt="image" src="https://github.com/user-attachments/assets/251ef989-6aa4-422d-8562-b005463b26b9" />

Ara el que farem sera crear un usuari amb useradd on tindrem que ficar la contrasenya amb passwd “nom usuari” i el canviar el sistema de la terminal 

<img width="542" height="130" alt="image" src="https://github.com/user-attachments/assets/30cda419-99f4-4e52-90c2-54a6ecc12db8" />

També crearem la carpeta de l’usuari on li assignarem els permisos corresponents

<img width="617" height="314" alt="image" src="https://github.com/user-attachments/assets/b60d335b-471b-48f3-9084-ebc5bd8e27dc" />

I si intentem iniciar gràficament com es pot observar si que podem

<img width="1281" height="800" alt="image" src="https://github.com/user-attachments/assets/15d2b41e-d232-4524-bb32-c944c87497b6" />

Si borrem un usuari amb deluser la única cosa que fa es el borrar la forma de iniciar graficament mentres que es manteneixen la carpeta de l’usuari amb tota la informació

<img width="658" height="179" alt="imagen" src="https://github.com/user-attachments/assets/86301b6e-4e0f-411f-b514-3a4dcf58d460" />

Mentres que si el borrem amb userdel -r  el que fa es el esborrar tot incluit carpeta

<img width="604" height="144" alt="imagen" src="https://github.com/user-attachments/assets/3ae21e83-b949-4c6d-8bd5-13cff0b4e6c6" />

Per a poder bloquejar un usuari del sistema sense borrar-lo usarem el usermod -L  

<img width="734" height="161" alt="imagen" src="https://github.com/user-attachments/assets/62eed601-6315-40b4-ac87-02d68d9edd64" />

Per a poder desbloqueijar usarem la mateixa comanda pero en aquest cas en comte de -L sera -U

<img width="751" height="98" alt="imagen" src="https://github.com/user-attachments/assets/6d58eb03-4fbd-4abc-a5fd-67004dff31ee" />

<img width="512" height="231" alt="imagen" src="https://github.com/user-attachments/assets/719dd854-b73a-4a7d-8d1e-381fdc9e2d1d" />

Tenim moltes formes d'afegir usuaris a un grup pero aquestes son les 3 que hem usat

<img width="535" height="184" alt="imagen" src="https://github.com/user-attachments/assets/0091cc5f-c7a3-4c4c-9c8d-bdbde40ee49a" />

Aquestes son dos maneres de borrar usuaris de un grup en especific

<img width="508" height="166" alt="imagen" src="https://github.com/user-attachments/assets/45ba0ea4-2241-4a4a-841f-4f5fd29022e6" />

Per natros canviar el grup principal d'un usuari o podem fer amb el usemod -g

<img width="508" height="166" alt="imagen" src="https://github.com/user-attachments/assets/06ff44c1-6ee2-435d-b6fd-f560e8e756d2" />

Per mirar de forma facil els grups d'un usuari podem usar el groups nom d'usuari

<img width="358" height="58" alt="imagen" src="https://github.com/user-attachments/assets/42948a61-4185-4bb9-8156-f0395a93a4e6" />

Per a borrar un grup usarem groupdel pero si aquest grup es el grup principal d'algun usuari tindrem que canviar els permisos per a que la carpeta principal sigui una altra

<img width="536" height="103" alt="imagen" src="https://github.com/user-attachments/assets/39882e49-195e-433f-a7ee-a58d205ad94d" />

Els arxius ocults son aquells que começen en un punt. I aquest fitxers estan 

<img width="640" height="399" alt="imagen" src="https://github.com/user-attachments/assets/8f3b19ee-3a41-423e-a419-e16e609feaea" />


<img width="588" height="220" alt="imagen" src="https://github.com/user-attachments/assets/e2fdc33c-3d6f-4bb8-9c4c-8da464645f84" />

Al editar aquest arxiu podem alterar el comprotament de la comanda adduser

<img width="736" height="440" alt="imagen" src="https://github.com/user-attachments/assets/5112e311-c15a-4b07-8979-af11407de29a" />

Aquest arxiu actua tant quan usem adduser com quan usem el useradd on un canvi que podem fer es el canviar el minim de dies de la contrasenya com els dies que tarda en avisrnos

<img width="736" height="440" alt="imagen" src="https://github.com/user-attachments/assets/5451f52b-c19a-4a78-9232-2265919bfc2d" />

Per a modificar unicament el comportament de la comanda de useradd entrarem al següent arxiu on el canvi que farem sera el canvi de /bin/sh a /bin/bash

<img width="736" height="440" alt="imagen" src="https://github.com/user-attachments/assets/c1a1cc99-1952-4ef0-8d65-7937153671ff" />

Com a comprovacions de els canvis que hem fet que afecta a la comanda adduser tot a funcionat

<img width="733" height="216" alt="imagen" src="https://github.com/user-attachments/assets/9d8bb60c-c94b-4ba6-a02d-060bdb940556" />

I com a comprovacions des canvis de la comanda useradd tambe a funcionat tot 

<img width="730" height="120" alt="imagen" src="https://github.com/user-attachments/assets/1f5f020a-51fe-4b05-82ce-ce7317bb51db" />

  - Canvis personals de adduser

Un canvi que faig es el que al crear un usuari automaticament el fique als grups que es mostren a continuacio

<img width="343" height="72" alt="imagen" src="https://github.com/user-attachments/assets/8109fcc6-f328-4f59-b14d-56b7a9d30533" />

Altres canvis es el canviar el rang de GID i UID 

<img width="243" height="198" alt="imagen" src="https://github.com/user-attachments/assets/c9ae2d1c-d1b2-4825-825f-fb755d6097e5" />

Aquest canvi es més que res per als dos tant com adduser com useradd i es el fet de que per a usar ls -la u podrem fer usant ll

<img width="758" height="108" alt="imagen" src="https://github.com/user-attachments/assets/849630f0-875a-4133-a61f-4f19aa8ab787" />

Tambe he volgut ficar aquest altre dins del .profile que el que fa es el mostrar el temps que porta enjagat i l'altre es un missatge que he volgut ficar jo

<img width="734" height="95" alt="imagen" src="https://github.com/user-attachments/assets/5362c1b5-b043-44fd-ab9c-182d06817bf9" />

Ara el que queda es comprovar que funcione tot

<img width="351" height="30" alt="imagen" src="https://github.com/user-attachments/assets/c5d026be-b6d3-4efa-ace4-ec03e7d61629" />

Al moment de crear l'usuari ens surtira el que l'usuari s'esta afegint als grups tot i que no em trova dos dels 3 grups

<img width="420" height="78" alt="imagen" src="https://github.com/user-attachments/assets/bfc991ae-88d2-411b-9df1-28e9a5b5b2d8" />

Com a primeres coses que podem observar al iniciar sessio es que al moment d'entrar si que apareixen els dos missatges que he ficat al .profile

<img width="717" height="691" alt="imagen" src="https://github.com/user-attachments/assets/b63dbb8d-0c75-45a8-ab71-d7d0147a3a8f" />

Tambe si fem ll es com si usesem ls -la 

<img width="599" height="203" alt="imagen" src="https://github.com/user-attachments/assets/67af1872-b1bc-4ad0-a8ee-7811e20e3217" />

Si anem a l'arxiu group podrem veure com si que esta dins del rang que li he asignat 

<img width="185" height="27" alt="imagen" src="https://github.com/user-attachments/assets/f4781099-ed2a-48e6-a162-4fff4e8b6074" />


  - Canvis personals de useradd

Dins del useradd per a començar el que he fet a sigut el que es cree el repositori home automaticament i no el tingues que crear tu manualment

<img width="543" height="82" alt="imagen" src="https://github.com/user-attachments/assets/2923c5fb-57c7-4455-b00f-a08112f73183" />

Tambe he ficat el que com a shell use el /bin/bash

<img width="702" height="132" alt="imagen" src="https://github.com/user-attachments/assets/a99e632d-7189-4841-8020-6eaccad3c223" />

Ara toca el comprovar si s'han aplicat els canvis

<img width="372" height="28" alt="imagen" src="https://github.com/user-attachments/assets/4162992d-1629-4db7-981a-6934fc1caf17" />

I si inciem sessio amb l'usuari podem veure el com si qeu tenim carpeta home

<img width="265" height="43" alt="imagen" src="https://github.com/user-attachments/assets/8a02816e-aa62-49f6-a6a6-8a10a2ec483f" />

## Gestio de permisos

Preparo l'entorn per als següents pasos

<img width="536" height="108" alt="imagen" src="https://github.com/user-attachments/assets/607215e3-d8a9-4e7d-aa20-6c7ff1ba846d" />

Crearem un grup on li ficarem de nom parchis alli afegirem dos usuaris 

<img width="546" height="231" alt="imagen" src="https://github.com/user-attachments/assets/594e3189-8d9f-429e-8b30-57b3934241b0" />

Aqui podem observar la carpeta nova que hem creat que es diu compartida amb tots els seus permisos de base

<img width="607" height="48" alt="imagen" src="https://github.com/user-attachments/assets/fb56a771-c258-46e7-b986-b34571943d9f" />

Aqui cambiem el propietari de la carpeta al igual que el grup propietari que sera parchis 

<img width="582" height="123" alt="imagen" src="https://github.com/user-attachments/assets/be4a3870-43ec-4ed2-a438-cf149906eaed" />

Ara cambiem els permisos de tal forma que altres usuaris no puguin accedir

<img width="553" height="77" alt="imagen" src="https://github.com/user-attachments/assets/74af09d8-04ef-45ac-9e1e-e9726e946c4e" />

L'usuari roig te tots els permisos

<img width="743" height="345" alt="imagen" src="https://github.com/user-attachments/assets/2f6447fc-a4d2-45a3-ae8d-74a6fd42546f" />

L'usuari blau pot entrar a la carpeta pero no pot ni crear ni eliminar arxiu

<img width="726" height="366" alt="imagen" src="https://github.com/user-attachments/assets/c295aa02-1fba-4393-8a9d-a5fbb10a3b0e" />

I l'usuari verd no te ningun permis aixi que no podra ni veure el contingut de la carpeta

<img width="734" height="342" alt="imagen" src="https://github.com/user-attachments/assets/0479175f-be43-47b9-ad4b-d4571b59f137" />

Per fer un usuari especial que no estigui dins del grup ni sigui el propietari pero inclus aixi tenir permisos es fa de la següent forma on es mostra com a una exepcio amb els permisos que te

<img width="729" height="241" alt="imagen" src="https://github.com/user-attachments/assets/6b4a1b6b-655e-4ea6-b8fb-5486e608383e" />

I com es pot observar si que te els permisos asignats

<img width="752" height="359" alt="imagen" src="https://github.com/user-attachments/assets/24e3261c-4497-4a5e-9f87-44c1b8aa10b4" />

Tambe es pot fer un usuari especial per a denegar permisos com ara es el cas de que un usuari que podia accedir a la carpeta no pugui ni accedir

<img width="725" height="357" alt="imagen" src="https://github.com/user-attachments/assets/f34c56bd-8641-4a9c-9efd-aaa6ec9fb323" />

I funciona

<img width="746" height="251" alt="imagen" src="https://github.com/user-attachments/assets/15d35b8f-38c8-4d37-812e-e57cd6c32737" />

Per a eliminar totes les exepcions que hem fet ara usarem el setfacl -b 

<img width="732" height="249" alt="imagen" src="https://github.com/user-attachments/assets/0fc9dee5-10c1-4571-b6bb-090e6b476a05" />

Per a crear una carpeta per a tots usarem l'asignacio de permisis root:root on tambe ficarem 777 per a que puguin fer de tot a la carpeta

<img width="709" height="147" alt="imagen" src="https://github.com/user-attachments/assets/b4570177-a805-4a3e-9d8b-2fca35e89e71" />

Necesitem que tot i que tenen tots els permisos nomes pugin esborrar lo seu i no el dels altres i es fara de la següent forma

<img width="701" height="116" alt="imagen" src="https://github.com/user-attachments/assets/d3b02bc9-b174-4683-83d8-e97ba22a512c" />

On com es pot comprovar no ens deixa borrar coses no creades per natros

<img width="719" height="349" alt="imagen" src="https://github.com/user-attachments/assets/d91d0966-274f-4807-ba0f-8db6868bbf8a" />



## Gestió de procesos



