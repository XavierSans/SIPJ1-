---
layout: default
title: "Sprint 1: Avaluació, Instal·lació i Configuració de Xarxes i Sistemes Operatius"
---

## Virtualització i insttal·lació del SO Ubuntu

Requisits minims:

<img width="901" height="555" alt="image" src="https://github.com/user-attachments/assets/7e13d384-ef23-428a-80a9-fc3b6b90898b" />

Implementació dels requisits:

<img width="585" height="654" alt="image" src="https://github.com/user-attachments/assets/070cb8d3-d6fa-4223-a14f-035483b141cc" />

## Proces d'instal·lació

<img width="723" height="402" alt="image" src="https://github.com/user-attachments/assets/e1a245e4-837e-4dd6-855b-d10c8f9b988d" />

<img width="876" height="677" alt="image" src="https://github.com/user-attachments/assets/74b1e7cc-b3a3-4971-9123-01edcab1905e" />

<img width="876" height="677" alt="image" src="https://github.com/user-attachments/assets/6bcf2cc7-d6bc-4322-9355-2325a9cfd5e9" />

<img width="876" height="677" alt="image" src="https://github.com/user-attachments/assets/44d7283b-1f68-4497-8c21-1a2478b9bccb" />

Necesitarem tirar l'opcio algo més per aixi accedir al menu de particions:

<img width="830" height="694" alt="image" src="https://github.com/user-attachments/assets/67073242-7d40-4de9-8270-aa514b215cff" />

Una vegada dins del menú de particions haurem d'agafar el volum del disc que hem creat i reservar l'espai per al qual millor ens convingué a nosaltres en el meu cas he fet un total de 4 particions en les quals he reservat 20 GB, ja que en l'arrel és on es conte el sistema, aplicacions i configuració bàsica i tot i que en menys també ja tenim suficient he ficat una mica més només per si tenim que instal·lar molt, la següent és el boot en 1GB li he ficat tant poc ja que te el kernel i arrencada inclòs en menys pot funcionar ja i amb el /home que en té 20 GB pel fet que conté totes les dades de l'usuari i si hi arriba a haver molt de contingut necessitaré molt d'espai i ja per últim tinc 4GB reservades per a la partició SWAP per tindre una ajuda extra en memòria virtual.

<img width="873" height="631" alt="image" src="https://github.com/user-attachments/assets/76c606b6-026d-4d6f-af0a-42f56f29cca6" />

<img width="830" height="694" alt="image" src="https://github.com/user-attachments/assets/e45a4422-9c3f-4ab3-a3d7-31fb1b5802c5" />

I ja u tenim instalat

<img width="1280" height="801" alt="image" src="https://github.com/user-attachments/assets/3d8d6114-b3b2-4c0a-a38a-6ed011d33b15" />

### Llincenciament

Captura de les llicencies que trovem a ubuntu:

<img width="648" height="426" alt="image" src="https://github.com/user-attachments/assets/dbdc4645-3fe6-40b9-ae37-3f255dd9813a" />

A continuació explicaré el perquè al directori /usr/share/common-licenses hi ha els textos legals de les llicències més típiques que fan servir els programes del sistema:

- GPL → la més usada a Linux, obliga a compartir el codi si el distribueixes.

- LGPL → com la GPL però més flexible per biblioteques.

- Apache / BSD / Artistic / MPL → més permissives, deixen barrejar amb programari privatiu.

- GFDL → per documentació.

- CC0 → domini públic (sense restriccions).

Per dir-ho d'una forma no hi ha ninguna principal però la més usada de les ja mostrades seria la GPL per el ja explicat.

## Instal·lacions duals i Gestors d'arrencada

<img width="876" height="604" alt="image" src="https://github.com/user-attachments/assets/6499d5a0-28d8-44c0-b7be-d16f3ab66a89" />

<img width="671" height="505" alt="image" src="https://github.com/user-attachments/assets/909e0f9f-e4c1-461e-a0f2-a243c5b2b812" />

<img width="643" height="482" alt="image" src="https://github.com/user-attachments/assets/9fffcca9-0353-4e83-bfc5-ef92ff3849bc" />

<img width="1028" height="774" alt="image" src="https://github.com/user-attachments/assets/613c5eb2-62e3-42f8-bf5e-899e6227c1a9" />

<img width="724" height="395" alt="image" src="https://github.com/user-attachments/assets/b1293120-3c3f-4c61-bfd5-90c4484599ad" />

<img width="724" height="395" alt="image" src="https://github.com/user-attachments/assets/1a616199-30cc-4274-9bf7-160b0b570e86" />

<img width="733" height="288" alt="image" src="https://github.com/user-attachments/assets/1aa8c9d5-9304-49e9-addb-aa2b20188a35" />

<img width="650" height="479" alt="image" src="https://github.com/user-attachments/assets/d57eaf06-8177-47b0-adda-7686b70cbfd8" />

<img width="1024" height="763" alt="image" src="https://github.com/user-attachments/assets/2fa89392-7c41-4d88-8cbf-774b1c6cebbc" />

##Instantanies

<img width="699" height="188" alt="image" src="https://github.com/user-attachments/assets/41ac3a56-4a61-49cf-9f14-c797eacd892d" />

<img width="728" height="506" alt="image" src="https://github.com/user-attachments/assets/a21491c4-33d1-4a58-a08b-5743c57eb6cb" />

<img width="564" height="141" alt="image" src="https://github.com/user-attachments/assets/c8caa1c1-0a6c-49c6-9efe-f6b694acf31e" />

<img width="788" height="321" alt="image" src="https://github.com/user-attachments/assets/6435689e-7b09-482c-978a-de56f2519b11" />

<img width="1030" height="411" alt="image" src="https://github.com/user-attachments/assets/6eff05aa-d934-4b83-851e-cf8a8af93dfc" />

<img width="98" height="131" alt="image" src="https://github.com/user-attachments/assets/2dd021c7-9038-4a4c-a822-6563ab56854b" />

<img width="723" height="292" alt="image" src="https://github.com/user-attachments/assets/af30218e-58ef-4efc-ae73-3e3097060410" />

<img width="609" height="677" alt="image" src="https://github.com/user-attachments/assets/d64cd697-4d09-4691-b659-83b78fa0031f" />

<img width="609" height="677" alt="image" src="https://github.com/user-attachments/assets/39ed51e0-0286-47c6-8452-9bdaed935fe8" />

<img width="609" height="677" alt="image" src="https://github.com/user-attachments/assets/df74da24-8e98-4e60-94f7-cf7160fa0221" />

<img width="757" height="701" alt="image" src="https://github.com/user-attachments/assets/30a04525-eaf3-473d-a532-2d1e83db4cd4" />

<img width="808" height="637" alt="image" src="https://github.com/user-attachments/assets/9c693ceb-b49f-4785-a96d-c0aee79da3b6" />

<img width="808" height="637" alt="image" src="https://github.com/user-attachments/assets/9fba7dad-88ef-4389-997b-f706d2c10185" />

<img width="643" height="96" alt="image" src="https://github.com/user-attachments/assets/9d1cc3c4-0764-47a3-b4eb-0cf2d51b6374" />

<img width="515" height="594" alt="image" src="https://github.com/user-attachments/assets/eeda8112-1fd3-4ff4-9cea-ccf0b648531e" />

<img width="1289" height="803" alt="image" src="https://github.com/user-attachments/assets/09c11cab-331e-4854-bd15-7ba9c9e75ffe" />

<img width="1289" height="803" alt="image" src="https://github.com/user-attachments/assets/7dda6fd9-0970-49cc-b29c-74eec31bee23" />

<img width="586" height="481" alt="image" src="https://github.com/user-attachments/assets/044c8ff0-c4f6-4274-a0c6-8cc3fc22e063" />

<img width="601" height="362" alt="image" src="https://github.com/user-attachments/assets/030f7b7c-e9d2-4162-960a-c74a9929ecc6" />

<img width="597" height="483" alt="image" src="https://github.com/user-attachments/assets/fd51c27f-18e5-4914-9eff-28e482e2ac4c" />

<img width="742" height="485" alt="image" src="https://github.com/user-attachments/assets/4fd1c3ac-132f-4c54-ba89-37e8913e484f" />

<img width="372" height="47" alt="image" src="https://github.com/user-attachments/assets/4eed1e66-6bb1-4c1a-be8a-5da50862a3e6" />

<img width="746" height="292" alt="image" src="https://github.com/user-attachments/assets/a7817fe0-a910-4e7a-90fa-e54010f9cc4f" />

<img width="746" height="292" alt="image" src="https://github.com/user-attachments/assets/9161332f-85b7-4031-a724-4f2ca3629802" />


## Particions i punts de restauració
## Configuració bàsica de la xarxa
## Comandes genrals i instal·lació d'aplicacions 
