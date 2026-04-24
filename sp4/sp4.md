---
layout: default
title: "Sprint 4: Monitorització, connexió remota i llicenciament"
---

## Monotoritzacio

auth      debug 
mail      infor
lpr       notice
kern      warning,warn
cron      err,error
....      crit
          alert
          emerg, panic

Dins del monitoreg del sistema podem veure tots els procesos que hi han en aquest moment poden matar els procesos que ocupin molt o dornar una preferencia major a altres

<img width="716" height="508" alt="imagen" src="https://github.com/user-attachments/assets/c0320bbb-26b7-480d-ac15-b5c6c12a89b9" />

<img width="716" height="508" alt="imagen" src="https://github.com/user-attachments/assets/187437ad-0616-43bd-bb03-b8e5b5935f95" />

<img width="716" height="508" alt="imagen" src="https://github.com/user-attachments/assets/b8a5aecb-a6f3-422a-89c1-ebe81301287d" />


## Syslog

Aqui es guarden diversos logs (registres) com autentificacio d'usuaris del sistema, kernell, el gran journal, etc. Coses que instal·lem, els seus logs es desen aqui
Diversos archis compartits aqui s'anmomenen "notacio de logs", ja que son tants que per espai i organitzacio es desen aixi

## lograte

Aqui es pot configurar la rotacio dels logs, cada quan volem registrar x event. En el seu directori hi ha arxius de configuracio per cada serveix

## rsyslog

50.default.conf

<img width="839" height="489" alt="imagen" src="https://github.com/user-attachments/assets/21bb2f09-ef66-4734-917b-c8c27dca711e" />

## Loger

<img width="799" height="97" alt="imagen" src="https://github.com/user-attachments/assets/c96291dc-9b49-4a6d-8718-888a8bcc2943" />

Ara el que farem sera el canviar el * del mail a "=crit":

<img width="828" height="448" alt="imagen" src="https://github.com/user-attachments/assets/662edf68-94db-4225-add3-b1c3b4f0b568" />

Cal fer un "sudo systemctl restart rsyslog.service".

I ara no s'ha desat el log amb .alert, sols el .crit:

<img width="762" height="250" alt="imagen" src="https://github.com/user-attachments/assets/ac3fa165-cdcb-443c-9605-f975daf1d399" />

## Xavier.log

<img width="762" height="250" alt="imagen" src="https://github.com/user-attachments/assets/adab31ba-e4ee-44ab-bce0-575171994c7d" />

<img width="1488" height="149" alt="Imatge enganxada (7)" src="https://github.com/user-attachments/assets/8f4675e5-389d-40c2-a531-0f3e2fb0ecf9" />

## Enviament de paquets amb dos maquines ubuntu

Primer que tot comprobem que hi hagui conexio amb les dos maquines

<img width="603" height="185" alt="imagen" src="https://github.com/user-attachments/assets/8cb1a3e5-0cd3-4396-aeb1-379b07453cfa" />

Despres de comprobar si tenim conexio anirem al arxiu de configuracio /etc/rsyslog.conf i al final de l'arxiu ficarem el següent

<img width="311" height="73" alt="imagen" src="https://github.com/user-attachments/assets/1b5b1539-518e-45f2-a833-cd1d216c7cfa" />

El següent pas sera el crear la carpeta on aniran els logs 

<img width="552" height="72" alt="imagen" src="https://github.com/user-attachments/assets/67b730dc-b49c-430d-ab70-710956f3ac65" />

I tambe configurarem els permisos necesaris per a la carpeta ja que si no despres donaran errors de creacio

<img width="630" height="55" alt="imagen" src="https://github.com/user-attachments/assets/b085bcbf-19da-4fb8-b331-8ff3692c2c3c" />

I com a ultima configuracio al servidor, configurarem el lloc on tenen que anar els logs que sera a la carpeta que hem creat 

<img width="609" height="126" alt="imagen" src="https://github.com/user-attachments/assets/2cc8dc59-9dca-448b-8ff3-b00d1395e6a9" />

I reinicem el servei

<img width="732" height="313" alt="imagen" src="https://github.com/user-attachments/assets/a66813bb-2976-409c-96da-9ca7e03b5474" />

I habilitarem el port del tcp al servidor

<img width="461" height="61" alt="imagen" src="https://github.com/user-attachments/assets/616a5f7b-fbb7-4cbf-a8b1-9685f6d0b9ac" />

Ara anirem al client on instalarem el rsyslog

<img width="730" height="401" alt="imagen" src="https://github.com/user-attachments/assets/7ffd6ad3-f092-44de-b2e3-452bcecf1342" />

<img width="703" height="180" alt="imagen" src="https://github.com/user-attachments/assets/d415877b-c0f1-4606-8317-362d3618b096" />


## SSH

<img width="562" height="45" alt="image" src="https://github.com/user-attachments/assets/1328e027-fc2b-48f7-9635-42284450e9b3" />

<img width="448" height="105" alt="image" src="https://github.com/user-attachments/assets/db6aa603-7e05-402a-95bd-7b6550be4fee" />

<img width="597" height="194" alt="image" src="https://github.com/user-attachments/assets/42ee6f4e-1dc5-4c9b-8503-b573ea6cc3b5" />

<img width="1538" height="385" alt="image" src="https://github.com/user-attachments/assets/6ecd415d-eedd-47d8-901f-ba49225775a1" />

<img width="1540" height="89" alt="image" src="https://github.com/user-attachments/assets/5bb51d44-3e54-4893-bc54-9f3c01253753" />

## VNC

<img width="646" height="167" alt="imagen" src="https://github.com/user-attachments/assets/9a2a8fed-087c-4cc1-b6c6-6ef8328c50b6" />

<img width="510" height="101" alt="imagen" src="https://github.com/user-attachments/assets/165fa688-aead-4375-b794-4cce367569ae" />

<img width="454" height="61" alt="imagen" src="https://github.com/user-attachments/assets/e948c624-21a7-4df0-948c-976b0f401067" />

<img width="651" height="219" alt="imagen" src="https://github.com/user-attachments/assets/b335a258-ce5a-4b4e-b1b8-114c97843d42" />

<img width="413" height="36" alt="imagen" src="https://github.com/user-attachments/assets/0f510401-f509-41ee-915c-231142b1befe" />

<img width="601" height="196" alt="imagen" src="https://github.com/user-attachments/assets/a161c5be-7486-4e15-873d-3e4dc26f3b3a" />

<img width="411" height="75" alt="imagen" src="https://github.com/user-attachments/assets/d0af8c06-3042-44db-98eb-c0387402b24c" />

<img width="601" height="196" alt="imagen" src="https://github.com/user-attachments/assets/7e9a299a-d8a0-4184-a296-ee5fc3acb2aa" />

<img width="1630" height="924" alt="imagen" src="https://github.com/user-attachments/assets/2cc40ebc-d052-4f7e-817e-dafe7a540f00" />

