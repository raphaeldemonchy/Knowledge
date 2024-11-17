# Linux

## TOOLS

sudo apt install inotify-tools
sudo apt install auditd

### Processus

*   `$> ps` : Commande pour afficher les processus en cours d'exécution

*   `$> ps aux` : Montre tous les processus, leur état, et les commandes qui les ont lancés

### Ressources

*   `$> top` : Affiche l'utilisation des ressources système en temps réel, y compris les processus qui consomment le plus le CPU

### Système

*   `$> strace -f -p <PID>` : Permet de suivre les appels système effectués par un programme

### Surveillance des Fichiers

*   `$> lsof -p <PID>` : Liste tous les fichiers ouverts sur le système

*   `$> inotifywait -m /path/to/directory` : Permet de surveiller les modifications de fichiers et de répertoires en temps réel

*   `$> auditctl -w path/to/file -p war` : Permet de surveiller les modifications de fichiers et de répertoires en temps réel

### Réseau
*   `$> netstat -tuln` : Utilisé pour observer les connexions réseau en cours

*   `$> iftop` : Affiche l'activité réseau en temps réel et montre quelles connexions sont utilisées par qu'elle processus

### Journaux Système

*   `$> tail -f /var/log/auth.log` : Contient les information d'auth, utile pour détecter des tentatives de connexion ou est escalades de privilèges

*   `$> tail -f /var/log/syslog` : Contient les information générales sur létat du système