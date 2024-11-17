# Windows

### Processus


*   `ps> Get-Process` : Affiche une liste détaillées des processus en cours d'exécution


*   `ps> Get-Process -Id <Id_Processus> | Format-List *` : Commande qui fournit tout les détails du processus


*   `ps> Stop-Process -Id <Id_Processus> -Force` : Terminer un processus suspect

### Réseau


*   `cmd> netstat -an` : Affiche toute les connexions réseau actives avec leur adresses IP et ports

*   `ps> Get-NetTCPConnection` : Fournit une vue détaillée des connexions TCP actives


*   `cmd> netstat -ano` : Permet d'identifier les processus utilisant des connexion réseau. Ajoutez le PID pour chaque connexion


*   `ps> Get-Process -Id <ID_Processus>` : Commande pour afficher les processus en cours d'exécution

### Système


*   `cmd> handle.exe -p <PID>` : Liste les fichiers ouvert par un processus

*   `ps> Get-Process -Id <PID> | ForEach-Object { $_.Modules }` : Affiche les modules et fichiers associés a un processus.

### Surveillance événement et journaux système

*   `ps> Get-EventLog -LogName System -Newest 10` : Filtre les journaux par nom (System, Security, Application, etc)

*   `ps> Get-WinEvent -LogName Security | Where-Object { $_.Message -like "*<nom_du_fichier>*" }` : Permet de rechercher les événements spécifiques contenant le nom du fichier

### Dump des informations avancées

*   `cmd> set` : Lister les variables d'environnement

*   `ps> Get-ChildItem Env:` : Lister les variables d'environnement

*   `cmd> tasklist /m` : Lister les DLL chargées par un processus

*   `ps> Get-Process -Id <PID> | ForEach-Object { $_.Modules }` : Montre les modules DLL chargés par les processus
