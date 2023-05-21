# Instalació i configuració d'un servidor FOG per Jan Plata

## Índex 

  - [1-Instalar i configurar un servidor FOG](#1-installar-i-configurar-un-servidor-fog)
  - [2-Capturar imatge des del client Ubuntu(iso personalitzada)](#2-capturar-imatge-des-del-client-ubuntuiso-personalitzada)
  - [3-Instal·lar imatge Ubuntu](#3-installar-imatge-ubuntu)
  - [4-Capturar imatge des del client Windows(iso personalitzada)](#4-capturar-imatge-des-del-client-windowsiso-personalitzada)
  - [5-Instal·lar imatge Windows](#5-installar-imatge-windows)
  - [6-Llençar un paquet per a que s’instal·li als clients fent servir snapin](6-llençar-un-paquet-per-a-que-sinstalli-als-clients-fent-servir-snapin)
 
    
## 1-Instal·lar i configurar un servidor FOG

Per a començar ens baixarem el servei FOG del repositori oficial del projecte FOG:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/11512a72-2ae3-473f-b488-ee7cf7075882)

Descomprimirem l’arxiu i accedirem a la seva ruta:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/387f31a8-f22c-4d07-abcb-865af2b3a844)

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/a066fd3a-5c89-4681-8c25-0e752ec20c3c)

Instal·larem el servei després de haberlo descarregat seguint els seguents passos:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/d73a8e23-8b7c-43fe-9eb5-cc4f1f0c7915)

Un cop hagi acabat la instal·lació del servei FOG al servidor podrem accedir a aquest desde el navegador amb la ip del servidor FOG amb les dades d'accés per defecte (user:fog , password:password) : 

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/1eb028f9-5752-4cb6-b396-369df958442b)

## 2-Capturar imatge des del client Ubuntu(iso personalitzada)
Com a primer pas instal·larem el navegador google chrome (o qualsevol software que vulguem incloure a la imatge del servidor) per a diferenciar aquesta imatge d'una imatge ubuntu generica

Un cop tinguem accés podrem crear les imatges al servidor a partir de la maquina client dirigint-nos al menú d’imatges i accedint a la secció de crear nova imatge:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/8b5d1320-4743-4336-89b1-bfab69136342)

Un cop fet aixó apagarem la màquina i configurarem la seva arrancada per xarxa:

(en el meu cas es fa desde la interficie de virtualbox pero podeu accedir a la BIOS per a configurar-ho en cas de fer-ho en màquina real)

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/0636d1bb-8c3f-4357-9399-760e44999a0e)

Un cop introduim la ip del servei tftp a la connexió per xarxa ens apareixera la següent pantalla i seleccionarem la opció de registrar el host i afegirlo a l’inventari:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/92e320c4-8b0f-4601-80df-68079c6d246f)

Un cop registrat el host podrem cambiar el nom de la imatge i assignar la imatge amb la que volem fer la captura al host:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/c671f049-c962-4d6d-8af7-98f5c55f3824)

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/5970b059-300d-4341-ad10-446112e71df6)

Un cop fet això podrem anar al menú de task>task management>list all hosts i manar la tasca del clonatge d’imatge al servidor:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/351f7048-0097-4cdd-826e-530b5d324565)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/848e2908-1d93-4333-ba35-394aecc7a583)

Reiniciarem la maquina per xarxa i esperarem a que acabi de clonar la imatge al servidor:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/05867c0e-4a9b-4c8f-92d6-03f42eaa69af)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/14ba9684-6c3a-4533-8929-b499e742a13c)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/bc49e894-5b25-4867-b588-fd6a04d2ddf4)

## 3-Instal·lar imatge Ubuntu

Un cop tinguem la imatge pujada al servidor podrem desplegarla a un equip client creant una tasca amb el botó de deploy de la imatge:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/c321db14-85ca-4b5e-a124-82ffdeb7c2bb)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/3cddddbf-8a65-44ae-b83a-557834794593)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/76ac56f1-6c4f-4543-bcda-59298e279b19)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/69bfe3f1-89d8-45bd-a520-a6dbe7ae3fe8)

Comprovació del client instal·lat correctament (podem veure que la imatge d'ubuntu te el google chrome preinstal·lat):

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/d990c56d-19c6-4b41-9056-c455b3571c14)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/768c8cdc-5c70-4eef-8681-0cb263e63c7c)

## 4-Capturar imatge des del client Windows(iso personalitzada)

Registrarem el host i la imatge del client de la mateixa manera que amb el client ubuntu i manarem la tasca de capturar la imatge:
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/b2a2dab4-c4c8-49bc-84be-72a4586838b7)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/fefef41d-ec1a-47db-b378-236a6460c1a8)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/5273ddcc-bfed-4c8e-a341-349a13f2403b)

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/4a9676a7-0aa7-483c-9c12-d72fa1d94d9c)

Finalment tindrem la nostra imatge clonada al servidor i preparada per a fer deploy al host desitjat:
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/33dba63f-5a59-46d1-8a2f-d850f06bc8fb)

## 5-Instal·lar imatge Windows

Un cop fet això podrem arrancar la maquina host per xarxa i seleccionar la imatge que volem :

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/c1592a2d-85e2-41ea-8d2e-6879521ab0f4)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/428b7009-42a8-42b7-95d1-33b436278997)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/8139e6e7-5b99-43d8-bdd9-0e4b3d4147ac)

Un cop acabat podrem veure el nostre client amb la iso personalitzada:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/153cce4b-f1e7-4fc2-9e2d-e50fead6cbca)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/4a92bafe-02ce-4c9c-b539-9cb23af2fc56)

## 6-Llençar un paquet per a que s’instal·li als clients fent servir snapin
En aquesta secció instal·laré google chrome de forma remota a un client windows fent servir les eines de snapin del servidor FOG, el primer que necessitarem sera el software que volguem afegir al client (en el meu cas el executable de l'instal·lador de google chrome enterprise).

El seguent pas serà descarregar i instal·lar el smartInstaller desde el client que vulguem gestionar:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/fc88e995-7d17-4c5a-8967-382b6dd22a93)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/a34aff4f-fead-436e-b866-0c3efd3a97be)

Crearem un script .bat que posteriorment afegirem al snapin i que executara l’instal·lador de chrome al client objectiu de forma automàtica:     
           
           - El script es el seguent: msiexec /i "C:\Archivos de programa (x86)\FOG\tmp\nom_snapin\nom_executable_afegit" /quiet

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/65679d27-7d63-4b32-ab2f-90444f0f67ba)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/0da7b96c-dca5-49ce-9bad-ba3530e6b821)

comprimirem l’instal·lador I el script en un zip per a afegir-lo al snappin pack al menu snapins>new snapin:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/118549cc-6c55-487a-882a-404935a8db93)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/2d7db04d-564d-4aa6-89e6-1a0999739cc8)

Un cop fet aixo associarem el snapin amb un host i crearem la tasca del snappin pack al menu de host> basic tasks > advanced > single snapins:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/053406d0-8955-4c74-9d94-2213e0fe3104)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/ed3daa7b-9435-468c-b07f-d1b6ac2612de)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/93682b05-b3af-4471-aaac-938d62281a80)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/dee495ce-4d00-4d70-a0ca-a2681b31e8fb)

Aixo manara una tasca per a executar el snapin al client(host) seleccionat I automaticament s’executara el nostre script .bat del arxiu comprimit per a instalar el navegador de google chrome:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/d3cff08f-3dfe-4aa4-977b-1aeb2ba60433)
![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/3b0f25b4-42a0-4aec-9332-4612d0b309cd)


