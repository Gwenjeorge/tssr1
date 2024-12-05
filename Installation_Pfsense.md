## INSTALLATION ET CONFIGURATION INITIALE DE PFSENSE

Nous allons dans un premier temps détailler l'installation de pfSense sur une machine qui doit initialement, au minimum, posséder deux interfaces réseaux.  
Nous verrons ensuite, en accédant à la webUI de pfSense, les configurations minimale à effectuer via le wizard d'installation.    

(config minmum? sur quel type d'hôte?)  

Nous devons posséder l'image de pfSense à installer, qu'il est possible de récupérer ici :  
Site officiel : https://www.pfsense.org/download/  
Site d'archive : https://repo.ialab.dsu.edu/pfsense/  

L'installateur de pfSense va, au démarrage, analyser la configuration matérielle de la machine hôte.  
Une fois cette analyse terminée l'assistant d'installation va, en mode console, vous guider pour les premières étapes.  
Acceptez les termes du contrat d'utilisation en appuyant sur Entrée  

![image](/pfSense_Install/1-Install.png)  

Sélectionnez "Install pfSense" et faîtes Entrée.  

![image](/pfSense_Install/2-Install.png)  

Concernant le mode de partitionnement, nous utiliserons le mode automatique (Auto-ZFS).   

![image](/pfSense_Install/3-Install.png)  

Valider ensuite le partionnement sans redondance.   

![image](/pfSense_Install/4-Install.png)  

Sélectionnez le disque dur avec Espace puis validez avec Entrée.  
Confirmer ensuite ce choix avec "Yes".  

![image](/pfSense_Install/5-Install.png)  
![image](/pfSense_Install/6-Install.png)  

pfSense va maintenant s'installer sur votre machine.  

![image](/pfSense_Install/7-Install.png)  

Lorsque l'installation est terminée, choisissez de redémarrer celle-ci.    

![image](/pfSense_Install/8-Install.png)  

Au premier démarrage, pfSense détecte automatiquement les interfaces réseau. 
La plupart du temps, vous verrez l'interface WAN rattachée à l'interface em0 correspondant à la première interface ajoutée. L'interface LAN quant à elle sera rattachée à l'interface em1, correspondant à la deuxième interface ajoutée à la VM.

![image](/pfSense_Install/9-Install.png)  

Comme on peut le voir, la configuration IP de l'interface WAN a été attribuée par le serveur DHCP de mon réseau. Nous allons configurer l'interface LAN avec sa configuration IP adéquate.

Pour modifier la configuration IP de notre interface LAN, nous allons procéder comme suit :
Choisissez l'option 2.
Ensuite, nous allons sélectionner l'interface LAN en entrant l'option 2 et indiquer que nous n'allons pas configurer l'interface via DHCP.
Enfin, nous allons définir la configuration IP de notre interface manuellement :
Adresse IP de l'interface LAN : 192.168.100.1
Masque de sous-réseau (en notation CIDR) : 24 = 255.255.255.0
Pas de passerelle
Pas de configuration IPv6
Pas de serveur DHCP IPv4 - il pourra être configuré par la suite depuis l'interface Web

![image](/pfSense_Install/10-Install.png)  


![image](/pfSense_Install/11-Install.png)  


![image](/pfSense_Install/12-Install.png)  


![image](/pfSense_Install/13-Install.png)  


![image](/pfSense_Install/14-Install.png)  


![image](/pfSense_Install/15-Install.png)  


![image](/pfSense_Install/16-Install.png)  


![image](/pfSense_Install/17-Install.png)  


![image](/pfSense_Install/18-Install.png)  


![image](/pfSense_Install/19-Install.png)  


![image](/pfSense_Install/20-Install.png) 


![image](/pfSense_Install/21-Install.png)  


