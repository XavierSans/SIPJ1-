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

<img width="742" height="347" alt="imagen" src="https://github.com/user-attachments/assets/f8d2ac24-f372-4d18-b8e8-bd71c05f6b1c" />

<img width="783" height="273" alt="imagen" src="https://github.com/user-attachments/assets/22007975-65ee-4b7b-92fa-5cd774777101" />

  - comandes

<img width="729" height="112" alt="imagen" src="https://github.com/user-attachments/assets/c4f50407-dcec-4335-bf93-0e013a23d3b4" />

<img width="735" height="441" alt="imagen" src="https://github.com/user-attachments/assets/f439395b-1fb2-42a2-920e-5c312e1bc629" />

<img width="741" height="214" alt="imagen" src="https://github.com/user-attachments/assets/3ccad7df-d911-46bc-95e9-fb7c2f0508e3" />

<img width="721" height="272" alt="imagen" src="https://github.com/user-attachments/assets/07debe5c-df52-4fca-8c44-637eba412bc4" />

<img width="587" height="80" alt="imagen" src="https://github.com/user-attachments/assets/d6efc12b-29c7-4241-b004-4de77176cfb2" />

<img width="608" height="371" alt="imagen" src="https://github.com/user-attachments/assets/80413fa7-54cf-42b7-b582-af69451f23ab" />

<img width="697" height="157" alt="imagen" src="https://github.com/user-attachments/assets/4d3d08bc-6a85-416b-b631-17a4170db071" />

<img width="743" height="354" alt="imagen" src="https://github.com/user-attachments/assets/589e1ca0-48b0-4913-b06c-1a0880ea4320" />

<img width="740" height="105" alt="imagen" src="https://github.com/user-attachments/assets/f396b665-4669-4512-a41c-a4a3ffaf75a3" />


## Còpies de seguretat i automització de tasques

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

<img width="542" height="130" alt="image" src="https://github.com/user-attachments/assets/30cda419-99f4-4e52-90c2-54a6ecc12db8" />

<img width="617" height="314" alt="image" src="https://github.com/user-attachments/assets/b60d335b-471b-48f3-9084-ebc5bd8e27dc" />

<img width="1281" height="800" alt="image" src="https://github.com/user-attachments/assets/15d2b41e-d232-4524-bb32-c944c87497b6" />

<img width="658" height="179" alt="imagen" src="https://github.com/user-attachments/assets/86301b6e-4e0f-411f-b514-3a4dcf58d460" />

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

    --Canvis personals de adduser

    
    --Canvis personals de useradd

## Gestió de procesos

