# OpenHabProject
Progetto domotica per controllo luci,temperatura e umidità da raspberry

## Intro 
OpenHabProject è un progetto domotico per uso domestico che permette accensione e spegnimento delle luci di casa, olte che rilevare temperatura e umidità   
IL progetto utilizza il progetto **Raspberry PI 3B+** e una scheda di relè  
Il software è basato su **OpenHabian** e **MQTT** (tramite Mosquito).  
l'attuazione dell'impianto avviene tramite il servizio cloud   
![OpenHab Screenshoot](https://image.ibb.co/eoFCVq/openhab-screen.png)  


# Hardware  
BOM (Bill of materials):
* Raspberry pi 3B+
* modulo relè optoisolato, con i numero di canali necessari  
* jumper dupont  
* pulsante 6x6mm

# Software    
Istruzioni per installazione:  

1. Installare OpenHabian seguendo la [guida ufficiale](https://www.openhab.org/docs/installation/openhabian.html#quick-start)  
1. Prima del primo avvio creare file (vuoto) `ssh` nella root della scheda sd, facnedo attenzione che non abbia nessuna estensione  
1. Trovare IP del Raspberry in rete e utilizzare ul Client SSH (_ad esempio PUTTY_) per connettersi. Per accedervi user `openhabian`
e pw `openhabian`.  
1. aggoirnare il sistema :
    ```
    sudo apt update 
    sudo apt upgrade
    ```
1. nealla cartella `/etc/openhab2/items` creare file `[user].items` dove si trovano le definizione dei pin con il relè deguendo il documento ufficiale
1. entrare nella cartella `/etc/openhab2/rules` creare file `[user].rules` dove si trovano le regole  seguendo ildocumento ufficiale 
