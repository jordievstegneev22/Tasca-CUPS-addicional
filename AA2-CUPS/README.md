# NF1.UD4. Compartició de recursos

## Presentació de l'activitat

Un cop assolit amb èxit el desplegament del servidor NFS, Devoptimize Solutions necessita la vostra proposta per centralitzar la impressió des de tots els equips.

Abans d'invertir en impressores de xarxa, el client vol veure una Prova de Concepte (*Proof of Concept*, PoC) que demostri que un servidor Linux pot gestionar una impressora i compartir-la de manera transparent amb els clients Zorin OS.

Per simular una impressora de xarxa sense necessitat d'adquirir maquinari físic, utilitzarem la impressora virtual **cups-pdf**. Aquesta eina funciona com una impressora convencional, però, en lloc d'imprimir el document en paper, genera un fitxer PDF que es desa al servidor.

L'objectiu és configurar aquest escenari i demostrar que un client pot enviar correctament un treball d'impressió al servidor.

## Durada de l'activitat

La durada prevista de l'activitat és 8 hores a classe.

## Objectius específics de l'activitat

- Configurar un servidor d'impressió utilitzant el protocol CUPS.

## Competències treballades

- **f)** Instal·lar, configurar i mantenir serveis multiusuari, aplicacions i dispositius compartits en un entorn de xarxa local, atenent les necessitats i els requeriments especificats.
- **g)** Realitzar proves funcionals en sistemes microinformàtics i xarxes locals, localitzant i diagnosticant disfuncions per comprovar-ne i ajustar-ne el funcionament.
- **o)** Utilitzar els mitjans de consulta disponibles, seleccionant-ne el més adequat en cada cas, per resoldre en un temps raonable supòsits no coneguts i dubtes professionals.

## Resultats d'aprenentatge i criteris d'avaluació

**RA4.** Gestiona els recursos compartits del sistema, interpretant especificacions i determinant nivells de seguretat.

- 4.4 Comparteix impressores en xarxa.

## Continguts

- 4.4 Configuració d'impressores compartides en xarxa.

## Capacitats clau treballades

- Autonomia
- Organització del treball
- Treball en equip
- Innovació
- Resolució de problemes
- Responsabilitat
- Relació interpersonal

## Enunciat de l'activitat

### Requeriments previs

Utilitzareu el mateix escenari configurat durant la PoC de NFS, de manera que podeu continuar treballant amb les mateixes màquines virtuals.

**Servidor:** Ubuntu Server configurat amb:

- Una interfície de xarxa en mode NAT.
- Una segona interfície de xarxa en mode Host-Only.

**Client:** Zorin OS Desktop, amb una configuració de xarxa compatible amb la del servidor per permetre la comunicació entre ambdues màquines.

### 1. Instal·lació de CUPS

- Instal·leu el servei CUPS al servidor.
- Documenteu les comandes utilitzades durant la instal·lació.

### 2. Instal·lació de la impressora virtual

- Instal·leu i configureu la impressora virtual cups-pdf al servidor.

### 3. Configuració de l'administració de CUPS

Configureu el servei CUPS per:

- Habilitar l'administració del servei.
- Permetre que CUPS escolti les connexions a través de totes les interfícies de xarxa necessàries.

Documenteu els canvis realitzats en la configuració.

### 4. Compartició de la impressora

Utilitzeu:

- El navegador web.
- La interfície web de CUPS.

Configureu la impressora perquè pugui ser compartida a través de la xarxa.

### 5. Configuració del client Zorin OS

- Des de la màquina client amb Zorin OS, afegiu la impressora compartida pel servidor.
- Comproveu que el client pot localitzar i utilitzar correctament la impressora.

### 6. Proves d'impressió

- Realitzeu proves d'impressió de diversos documents des del client.
- Comproveu que els treballs són enviats correctament al servidor d'impressió.

### 7. Comprovació dels documents generats

- Des del servidor, verifiqueu que s'han generat correctament els fitxers PDF corresponents als treballs enviats des del client.
- Documenteu:
  - La ubicació dels fitxers generats.
  - Els documents creats.
  - Les proves realitzades.

## Què cal lliurar?

Cal documentar:

- Les comandes utilitzades.
- Els canvis de configuració realitzats.
- Les proves efectuades.
- Les captures de pantalla necessàries per demostrar el correcte funcionament de la prova de concepte.

El format de lliurament serà Markdown, amb una carpeta al repositori indicat pel professorat amb la següent estructura:

```
.
├── README.md
├── AA2-CUPS.md
└── images/
    ├── screenshot1.png
    └── screenshot2.png
```

On `README.md` contindrà l'enunciat de l'activitat, `AA2-CUPS.md` serà el fitxer principal amb la descripció de l'activitat i les captures de pantalla es guardaran a la carpeta `images/`.

## Material de suport

- Material propi del mòdul. [NF1.UD4.A2 Compartició impressores (CUPS)](https://github.com/SMX-SOX/Materials/blob/main/NF1_SOX_Linux/UD4_Compart_Recursos/A2-CUPS.md)
- Sarah L. [How to Set Up CUPS Print Server on Ubuntu: The Definitive Guide (2026)](https://www.fosslinux.com/61850/how-to-set-up-cups-print-server-on-ubuntu.htm). FOSS Linux, Juny 2026.
- P. Ruiz. [Instalar una impresora virtual en Ubuntu 22.04 LTS](https://somebooks.es/instalar-una-impresora-virtual-en-ubuntu-22-04-lts/). Somebooks.es, Agost 2023.
