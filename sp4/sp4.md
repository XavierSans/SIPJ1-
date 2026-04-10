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

