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

<img width="425" height="261" alt="imagen" src="https://github.com/user-attachments/assets/f1eed315-c514-4e5b-8483-8174a53eda31" />

<img width="697" height="157" alt="imagen" src="https://github.com/user-attachments/assets/4d3d08bc-6a85-416b-b631-17a4170db071" />

<img width="743" height="354" alt="imagen" src="https://github.com/user-attachments/assets/589e1ca0-48b0-4913-b06c-1a0880ea4320" />

<img width="740" height="105" alt="imagen" src="https://github.com/user-attachments/assets/f396b665-4669-4512-a41c-a4a3ffaf75a3" />


## Còpies de seguretat i automització de tasques

## Gestió d'usuaris, grups i permisos

## Gestió de procesos

