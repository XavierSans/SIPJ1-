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



## Syslog

Aqui es guarden diversos logs (registres) com autentificacio d'usuaris del sistema, kernell, el gran journal, etc. Coses que instal·lem, els seus logs es desen aqui
Diversos archis compartits aqui s'anmomenen "notacio de logs", ja que son tants que per espai i organitzacio es desen aixi

## lograte

Aqui es pot configurar la rotacio dels logs, cada quan volem registrar x event. En el seu directori hi ha arxius de configuracio per cada serveix

## rsyslog

50.default.conf


