# Instalació i configuració d'un servidor FOG per Jan Plata

## Index 

    1- Instal·lar i configurar un servidor FOG
    2- Capturar des del client un Windows
    3- Capturar des del client un Ubuntu
    4- Instal·lar imatge Windows
    5- Instal·lar imatge Ubuntu
    6- Llençar un paquet per a que s’instal·li als clients
    
## Instal·lar i configurar un servidor FOG

Ens baixarem el servei FOG del repositori oficial del projecte FOG:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/11512a72-2ae3-473f-b488-ee7cf7075882)

Descomprimirem l’arxiu i accedirem a la seva ruta:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/387f31a8-f22c-4d07-abcb-865af2b3a844)

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/a066fd3a-5c89-4681-8c25-0e752ec20c3c)

Instal·larem el servei després de haberlo descarregat seguint els seguents passos:

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/d73a8e23-8b7c-43fe-9eb5-cc4f1f0c7915)

Un cop hagi acabat la instal·lació del servei FOG al servidor podrem accedir a aquest desde el navegador amb la ip del servidor FOG amb les dades d'accés per defecte (user:fog , password:password) : 

![image](https://github.com/GitJanPlata/Instalacio_FOG/assets/96839905/1eb028f9-5752-4cb6-b396-369df958442b)

## Capturar des del client un Ubuntu(iso personalitzada)

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



