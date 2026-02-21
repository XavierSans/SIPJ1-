---
layout: default
title: "Sprint 3: Gestió de dominis i Accesos"
---

## Instalació doini Ldap i Unir clients al domini

A les dos maquines ficarem de xarxa NAT

<img width="921" height="589" alt="imagen" src="https://github.com/user-attachments/assets/3d0795c3-0c79-4d5d-bf80-8e77766b4481" />

Li canviarem a les maquines de IP per DHCP a IP fixa manualment

<img width="921" height="589" alt="imagen" src="https://github.com/user-attachments/assets/3a00524f-a11e-46dd-b00b-15129db985c7" />

I probarem de fer ping a 1.1.1.1 on funciona

<img width="598" height="315" alt="imagen" src="https://github.com/user-attachments/assets/f2ad1701-ac7b-4f5f-9c2c-e1db80bfca74" />

Canviarem el hostname a un que natro vulguem

<img width="1026" height="93" alt="imagen" src="https://github.com/user-attachments/assets/535b01c8-391f-432e-87d5-49777d050ffd" />

I dins del arxiu /hosts ficarem la IP del nostre servidor més el hostname.domini del ldap que tenim pensat ficar

<img width="1026" height="93" alt="imagen" src="https://github.com/user-attachments/assets/f54ee647-3fd9-444e-869a-c7b2f109658f" />

Ara toca instalar el servei ldap usant la comanda que es mostra a continuacio

<img width="1026" height="374" alt="imagen" src="https://github.com/user-attachments/assets/7db6cb3f-54a5-4e97-ba45-0547fc415e64" />

Ens demana ficar una contrasenya i despres confirmar-la

<img width="1154" height="218" alt="imagen" src="https://github.com/user-attachments/assets/fed6f0a1-0f37-413e-a0cc-6a1b59ff1c66" />

I si fem un sudo slapcat podrem observar que ja tenim creat un domini

<img width="483" height="277" alt="imagen" src="https://github.com/user-attachments/assets/5c357d20-d8bc-4e4c-89ad-eec66b4b7e8c" />

Desde el moodle ens descarregarem un arxiu el qual conte usuaris per al ldap

<img width="677" height="255" alt="imagen" src="https://github.com/user-attachments/assets/cca1f2b3-ca12-47ed-836a-3b13e59421ae" />

Oviament antes hem definit el nom que voldrem per al domini al hosts ara toca definirlo pero al servei ldap i aixo ho farem usant un dpkgreconfigure on podrem començar amb la configuracio real

<img width="677" height="255" alt="imagen" src="https://github.com/user-attachments/assets/94e2cf50-5479-48d8-9067-6b5ca14d7c06" />

Aqui fiquem el nom del domini d'antes però sense el cat

<img width="857" height="257" alt="imagen" src="https://github.com/user-attachments/assets/5d21c73c-3e3f-4f15-b70c-0bdc89d2a710" />

I tornarem a ficar contrasenya i confirmar-la

<img width="857" height="257" alt="imagen" src="https://github.com/user-attachments/assets/4a2b6cfe-e574-4fa7-bc0f-4ea7bcccb90e" />

Borrarem l'anterior base que teniem que era la predeterminada

<img width="857" height="257" alt="imagen" src="https://github.com/user-attachments/assets/1dd3f7d0-36d8-4ef0-9a0b-c462a656eec1" />

I tornarem a donar que si

<img width="1817" height="276" alt="imagen" src="https://github.com/user-attachments/assets/f6e9f71e-72d9-4d27-bec0-beec58f1a6ea" />

I ja ho tenim el nostre domini gina.cat creat

<img width="470" height="265" alt="imagen" src="https://github.com/user-attachments/assets/9f0831cc-b6ea-409d-a483-359cafb3ca50" />

Ara anirem a cada un dels fitxers que ens hem descarregat antes i canviarem el domini per a que sigui igual que el que tenim 

<img width="370" height="145" alt="imagen" src="https://github.com/user-attachments/assets/92890bed-70de-4fa3-9876-693f3ba0c590" />

Aqui tambe ho farem

<img width="370" height="145" alt="imagen" src="https://github.com/user-attachments/assets/5ab5ac60-1de5-49bb-8066-b5627a2452ed" />

I aqui tambe

<img width="365" height="386" alt="imagen" src="https://github.com/user-attachments/assets/04c16cff-3a1b-4897-9a41-4f29aafa3147" />

I afegirem la informacio dels arxius al nostre ldap

<img width="896" height="249" alt="imagen" src="https://github.com/user-attachments/assets/63e5410c-1ebb-4beb-8500-db142c768a7f" />

I si tornem a fer un slapcat veurem la diferencia

<img width="578" height="829" alt="imagen" src="https://github.com/user-attachments/assets/9018a5ac-4404-4920-b050-2457cf10d3b1" />

Ara anem al client el primer que farem sera comprovar si podem fer ping amb el servidor

<img width="579" height="248" alt="imagen" src="https://github.com/user-attachments/assets/a126a818-1bd0-4fbf-bc0d-ac5fa9fdeb28" />

I ara instalarem les eines per a poder conectar el client al servidor ldap

<img width="708" height="43" alt="imagen" src="https://github.com/user-attachments/assets/ea55fb34-9c68-4326-8fdf-7b39f4898ff5" />

Aqui ficarem la IP del servidor

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/5dc24ea9-eb70-4d45-b10a-8843154144b8" />

I aqui el domini

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/5b9fcc5c-d534-47cd-b07f-c6e6f7248302" />

Triarem la versio 3

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/e5251f55-d0a1-453b-b17a-a0df1b2829e4" />

I aqui clicarem que si

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/3b255b5a-0cf0-4562-b203-91caf6c4578c" />

I aqui tambe

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/f91aac63-d644-4133-8561-bbe3c4b93d82" />

Aqui farem el mateix que antes de ficar el domini pero amb el cn=admin per a comptes privigeliats 

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/36971770-0e3c-48e0-808c-049c367a6558" />

I torem a ficar contrasenya

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/6c16921a-1973-4a7d-8cc2-8c8ca70a9fcc" />

Aqui tot i que seria per als usuaris no privilegiats ficarem el mateix 

<img width="736" height="444" alt="imagen" src="https://github.com/user-attachments/assets/7c238e49-c7e8-4ae1-b613-12d1edd7a754" />

I una altra vegada la contrasenya

<img width="739" height="448" alt="imagen" src="https://github.com/user-attachments/assets/63cef910-f8e5-4c4b-9ef4-7986f9faad42" />

Ara anirem al arxiu nsswitch.conf i el deixarem igual que en la imatge següent:

<img width="739" height="448" alt="imagen" src="https://github.com/user-attachments/assets/ec6ee978-0626-4049-869a-efba395b416d" />

I el mateix amb el common-session

<img width="739" height="448" alt="imagen" src="https://github.com/user-attachments/assets/27dba938-0cda-4bdd-8975-0e5c3a67ae09" />

I common-password no tenim que afegir res nomes tenim que eliminar parts de l'arxiu de tal forma que quedi aixi

<img width="998" height="448" alt="imagen" src="https://github.com/user-attachments/assets/130c5c64-9bb1-4849-bdb8-9b76935264bd" />

I l'ultim arxiu que tindrem que tocar sera 50-ubuntu.conf el qual tambe el tenim que deixar de la mateixa forma que com es mostra

<img width="690" height="108" alt="imagen" src="https://github.com/user-attachments/assets/bd129eb2-f8b3-4478-9c3d-9b86b5994233" />

Ara comprovem que el client pugui llegir els usuaris amb un grep alu1 i com es pot veure si que mostra algo

<img width="605" height="46" alt="imagen" src="https://github.com/user-attachments/assets/43ba9265-9b2e-426e-954e-d06bc7267f59" />

Si intentem iniciar sessio a partir de terminal tambe ens deixa

<img width="348" height="64" alt="imagen" src="https://github.com/user-attachments/assets/449529d6-8cae-41a0-9a34-3f6a38fa81f3" />

Creant la home com hem especificat als arxius

<img width="206" height="82" alt="imagen" src="https://github.com/user-attachments/assets/efaa16bf-8765-4a34-95ea-e5a76ff45269" />

I tambe podrem accedir graficament

<img width="572" height="388" alt="imagen" src="https://github.com/user-attachments/assets/8c59fd74-a423-4f2e-8218-9df0fc7bd2d4" />

### Fitxers ldif i comandes ldap

Per a fer les activitats farem un reconfigure per a borrar totes les dades que teniem antes i aixi no tenir interferencies i usant un arxiu del moodle afegirem nous usuaris i grups 

<img width="997" height="331" alt="imagen" src="https://github.com/user-attachments/assets/5fb1b0d4-359e-4353-b5ed-111f6aa410ac" />

1.

Com a primera activitat crearem un nou usuari creare un nou fitxer i ficare la info alli

<img width="1105" height="292" alt="imagen" src="https://github.com/user-attachments/assets/4f7e2d0f-c90a-47eb-9498-a5a32217cdd6" />

L'afegirem al domini de la mateixa forma que tots els altres

<img width="845" height="106" alt="imagen" src="https://github.com/user-attachments/assets/e293ebe0-55ac-4a28-84a1-fe417ef50099" />

2.

Com a segona activitat crearem una nova ou que li fiquem de nom nomines 

<img width="480" height="134" alt="imagen" src="https://github.com/user-attachments/assets/a6996fd1-f28c-41fe-8ac7-de90b7de877b" />

I fem el mateix que entes

<img width="807" height="69" alt="imagen" src="https://github.com/user-attachments/assets/a34cee34-2fb3-42be-aac8-09005306dc90" />

3.

Aqui no afegirem res si no modificarem creem un nou arxiu per aixi poder ficar al usuari david a la nova ou que hem creat

<img width="401" height="135" alt="imagen" src="https://github.com/user-attachments/assets/03176689-9f3c-4d80-b738-d77945c63cd6" />

En comptes del ldapadd usarem ldapmodify que tal i com u diu lo seu nom serveix per a modificar en comptes de per afegir

<img width="827" height="75" alt="imagen" src="https://github.com/user-attachments/assets/1b2cbf1f-db3a-4fc7-90ce-efb3cda00f01" />

I comprovem que estigui afegit

<img width="477" height="403" alt="imagen" src="https://github.com/user-attachments/assets/819a2ce7-ba19-45db-93a4-5cc55dfea81a" />

4.

Aqui farem una consulta per a mirar quans de grups tenim donan un total de 2

<img width="878" height="602" alt="imagen" src="https://github.com/user-attachments/assets/258b06e6-1588-44a8-b00d-eb94113df409" />

5.

Ara l'usuari que hem creat antes el ficarem a un d'aquests 2 grups

<img width="528" height="112" alt="imagen" src="https://github.com/user-attachments/assets/9c3a7873-adb4-4935-905f-c4536bf23707" />

I l'afegirem al grup usant el ldapmodify

<img width="867" height="77" alt="imagen" src="https://github.com/user-attachments/assets/d572e203-bfc8-4d5b-8c06-4ccf361af3af" />

6.

Aqui el que farem sera el canviar el congnom a l'usuari Sergi 

<img width="448" height="179" alt="imagen" src="https://github.com/user-attachments/assets/cf340d5d-ea8e-4c49-b653-6af215edef04" />

I aqui tornarem a un fer un ldapmodify i ens o accepta

<img width="917" height="71" alt="imagen" src="https://github.com/user-attachments/assets/e433faac-5cc8-4f1e-a8db-c529d04e1516" />

7.

Ara mirarem quants usuaris hi han dins de la uo rrhh que hi han un total de 3 usuaris 

<img width="942" height="521" alt="imagen" src="https://github.com/user-attachments/assets/06a24dfd-05c5-417b-99ca-a2caff522684" />

8.

No es pot ja que el posixgroup depen de ell 

<img width="893" height="103" alt="imagen" src="https://github.com/user-attachments/assets/d940070f-d2f3-47ea-b518-fff3ace2cad7" />

9.

Hi han un total de 3

<img width="1115" height="60" alt="imagen" src="https://github.com/user-attachments/assets/dfc62105-2624-43c3-bb84-44f63f319d32" />

10.

Aqui canviarem el nom del usuari Xavier a Francesc Xavier per a fer aixo tindrem que modificar el cn 

<img width="394" height="134" alt="imagen" src="https://github.com/user-attachments/assets/3cc2312f-5a87-4c4b-aa01-482e8cdea3e4" />

I amb un ldapmodify ja u tindrem

<img width="822" height="61" alt="imagen" src="https://github.com/user-attachments/assets/dd3e9387-17db-4be6-b80f-7153d8942ec0" />

Com es pot observar si que a canviat el cn 

<img width="462" height="395" alt="imagen" src="https://github.com/user-attachments/assets/39a60400-b9b7-4387-be67-a1ab99b4be6c" />

11.

Aqui tinderm que esborrar la uo nomines pero hi ha un problema i es que tenim un usuari dins d'aquesta uo aixi que tenim dos formes o eliminar les dos de una o canviar la uo del usuari jo he triat la segona opcio

<img width="393" height="114" alt="imagen" src="https://github.com/user-attachments/assets/db1f532b-1bc0-48a2-92a9-69ff92f32390" />

Fem un ldapmodify per canviar la uo

<img width="860" height="88" alt="imagen" src="https://github.com/user-attachments/assets/2afb7afd-a7f6-4ec4-8e43-3bc4ab2c3508" />

Com podem observar si fem una busqueda de a quina uo pertany david ficara que pertany a la rrhh

<img width="785" height="353" alt="imagen" src="https://github.com/user-attachments/assets/723247e0-e7b7-40ed-84a5-0343bb693009" />

I ara si que eliminem la uo de nomines

<img width="925" height="300" alt="imagen" src="https://github.com/user-attachments/assets/5f34d219-d28c-4feb-8115-8e2ea100b50a" />

12.

Aqui mostrem els usuaris que tinguin com a grup principal el grup administració

<img width="851" height="476" alt="imagen" src="https://github.com/user-attachments/assets/bd895b78-d4ba-4ffb-b32d-99cc041fdaa0" />

13.

L'usuari que te el uidNumber 1003 es l'usuari que he creat jo que es David

<img width="850" height="365" alt="imagen" src="https://github.com/user-attachments/assets/bfd9226e-e1c2-4dd9-9140-0f396ac1de4d" />

14.

No existeix cap usuari que començe per R i al mateix temps tingui el uidnumber=1004

<img width="1014" height="265" alt="imagen" src="https://github.com/user-attachments/assets/dd62a374-28d7-4573-8cc1-21a2a7831138" />

15.

Aqui mostrara al usuari sergi ja que forma part del grup informàtic i te de congnom pallares

<img width="1340" height="375" alt="imagen" src="https://github.com/user-attachments/assets/72b0bc64-bc01-48cf-8b71-255cd255f1d1" />


### Servidor samba i NFS

## Samba

Serveixen per a compartir fitxers o recursos a mes samba et deixa compartir impresores i fer la autenticacio al LDAP. NFS ho fa a partir de IP

El primer que farem sera anar al servidor i instalar el servei samba

<img width="736" height="441" alt="imagen" src="https://github.com/user-attachments/assets/a7100f8f-8633-402e-a20c-f5c875836538" />

Ara crearem una carpeta i ficarem un arxiu amb els permisos corresponents 

<img width="640" height="255" alt="imagen" src="https://github.com/user-attachments/assets/3eda94a4-ddac-4808-856a-4286964d6c42" />

I crearem uns quants ususaris que usaram per a les probes

<img width="623" height="153" alt="imagen" src="https://github.com/user-attachments/assets/5ddc0a46-b39c-4811-84d4-2825b23340c7" />

Registrarem cada usuari el samba ficant una contrasenya a cada un

<img width="443" height="250" alt="imagen" src="https://github.com/user-attachments/assets/97858a33-ed50-44da-9d0b-4a7ef96806fe" />

I crearem un grup que li direm colors on nomes afegirem a 2 dels 3 usuaris a roig i groc

<img width="443" height="250" alt="imagen" src="https://github.com/user-attachments/assets/98aed423-e5c8-43cb-9fc2-dfa285fd4827" />

I dins de l'arxiu de configuracio samba afegirem la següent informacio que seria a quina carpeta ens referim per a els següent permisos que es la de proves, que pugui permetre a usuaris invitats i com apartat més important tenim el que fiquem a read list l'usuari blau i el grup colors on estan roig i groc pero despres fiquem que blau tambe pugui escriure i per ultim que l'usuari roig no pugui ni entrar

<img width="296" height="207" alt="imagen" src="https://github.com/user-attachments/assets/2d54f827-13c3-4865-ae29-82917ee6cf28" />

Reiniciem el servei i comprovem que tot funcione be

<img width="1132" height="773" alt="imagen" src="https://github.com/user-attachments/assets/893953d3-c721-4ec5-9f7c-3aa598062c4f" />

Ara toca anar al client i instalar les eines per a conectar-nos al servidor samba 

<img width="708" height="421" alt="imagen" src="https://github.com/user-attachments/assets/80ad4f60-2737-4e9a-a3db-f8dd3f64a9dc" />

Si anem a la carpeta i fiquem smb://IP_SERVIDOR/CARPETA si ho hem fet tot be ens tindra que conectar 

<img width="708" height="421" alt="imagen" src="https://github.com/user-attachments/assets/fcdd42f5-8707-4ce0-b36e-e3d6ac573a31" />

On si intentem entrar en usuar invitat ens deixa entrar pero no ens deixa fer res més

<img width="708" height="421" alt="imagen" src="https://github.com/user-attachments/assets/28467a4e-cde1-48ee-b33e-f66f2b3fc878" />

En l'usuari blau tambe ens deixa entrar

<img width="708" height="421" alt="imagen" src="https://github.com/user-attachments/assets/b9c52c68-de5f-4ca7-8f14-477b8190dd20" />

I podem fer tot

<img width="660" height="244" alt="imagen" src="https://github.com/user-attachments/assets/e06b17e1-5cc9-4229-9bcc-406f0d0dfd54" />

En l'usuari groc podem entrar

<img width="676" height="511" alt="imagen" src="https://github.com/user-attachments/assets/411bdc6d-c0c8-4049-8915-7a17c7f6873a" />

Però no podem editar res

<img width="676" height="511" alt="imagen" src="https://github.com/user-attachments/assets/d306f8b6-778a-4d2e-ac83-6c63f5a85b15" />

I en l'usuar roig directament no podem ni accedir 

<img width="676" height="511" alt="imagen" src="https://github.com/user-attachments/assets/507f2a82-62a0-4cb1-8700-3322e3434040" />
<img width="676" height="511" alt="imagen" src="https://github.com/user-attachments/assets/361bec43-c630-4fee-8bf7-b284d9db4bfe" />

## NFS

NFS per compartir carpetes dins d'una xarxa interna i la idntificacio se fa nivell de maquina per host

Ara tornem al servidor on instalem les eines nfs

<img width="880" height="261" alt="imagen" src="https://github.com/user-attachments/assets/df068ca3-dc92-4c3a-8814-017c320c57d9" />

I comprovem l'estat del servei

<img width="862" height="213" alt="imagen" src="https://github.com/user-attachments/assets/c9aa8ce6-1b75-46af-a8d7-7bf8f840a1fb" />

Creem la carpeta que usarem per a les probes i li ficarem els permisos necesaris

<img width="638" height="135" alt="imagen" src="https://github.com/user-attachments/assets/4d4ce87d-74e9-44b0-b949-da2e2791c49f" />

Una vegada creada la carpeta anirem al etc/exports i ficarem el següent 

<img width="1034" height="240" alt="imagen" src="https://github.com/user-attachments/assets/ba68498a-456f-47ef-8402-697ab70aab77" />

Ara ens anem al client on instalarem les nfs-common

<img width="707" height="341" alt="imagen" src="https://github.com/user-attachments/assets/9f49edd6-5eef-4c45-a7ee-429bb3d7792c" />

I habilitarem la opcio que ens surt

<img width="1817" height="277" alt="imagen" src="https://github.com/user-attachments/assets/2a4a929b-51d0-4694-927e-ff5af3bfaf90" />

Crearem una carpeta i ficarem els permisos necesaris

<img width="340" height="70" alt="imagen" src="https://github.com/user-attachments/assets/8bcc2ccd-eb8e-47be-862a-d1e0935c00f3" />

Ara anirem al etc/fstab i ficarem la linia que es mostra

<img width="1057" height="281" alt="imagen" src="https://github.com/user-attachments/assets/a0b8de80-0af7-459d-9600-b7b364e738cf" />

Ara podem veure que dins la carpeta divendres tenim un arxiu prova aixi que com a comprovacio de que tot esta conectat tambe crearem un arxiu

<img width="345" height="79" alt="imagen" src="https://github.com/user-attachments/assets/5ffb5735-0282-4c47-b9a2-70dcba96729f" />

I al servidor tambe apareix

<img width="363" height="69" alt="imagen" src="https://github.com/user-attachments/assets/d9186174-9e04-41e7-8730-960639aa6773" />

Crearem una nova carpeta que li fiquem perfils i copiarem i pegarem la mateixa linia que tenim al fstab pero canviant els noms de les carpetes per /perfils

<img width="1134" height="271" alt="imagen" src="https://github.com/user-attachments/assets/b1598838-38b2-49ef-b501-7bf7ff52505a" />

I al exports farem el mateix

<img width="1134" height="271" alt="imagen" src="https://github.com/user-attachments/assets/8dfc3e44-cf30-4b28-b66d-08518c7ecbd5" />

Afegirem un usuari ldap pero que es creara en comptes de a la /home es creara a /perfils

<img width="908" height="296" alt="imagen" src="https://github.com/user-attachments/assets/36863dd5-fc30-4b89-ad76-e960966b1cc4" />

L'afegim 

<img width="365" height="409" alt="imagen" src="https://github.com/user-attachments/assets/243599d3-cd7e-409c-8b2e-fbf018f4da23" />

I podem iniciar sessio graficament 

<img width="916" height="70" alt="imagen" src="https://github.com/user-attachments/assets/d7b7d3fe-dc15-458c-a86d-2b036845bc79" />

I si anem al servidor i fem un ls /perfils/alu3 ens mostra la tipica informacio que apareix en la home

<img width="502" height="136" alt="imagen" src="https://github.com/user-attachments/assets/b29ab6da-3c3a-4d28-8f11-4e82ac33998c" />



<img width="577" height="503" alt="imagen" src="https://github.com/user-attachments/assets/aa3719f6-b5be-4a4c-9d3d-67daf8640ea0" />

<img width="627" height="466" alt="imagen" src="https://github.com/user-attachments/assets/437f0239-df97-4b10-9b93-c48a5019e013" />

<img width="461" height="92" alt="imagen" src="https://github.com/user-attachments/assets/ef60a252-e5ba-4197-8e63-005e8b498304" />

<img width="689" height="205" alt="imagen" src="https://github.com/user-attachments/assets/6b7fa1d4-8869-45d0-b12e-853820934e81" />

