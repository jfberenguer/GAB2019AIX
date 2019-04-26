# GAB2019AIX

# Monitoring Azure

Hands On Labs - Global azure Bootcamp 2019 - Aix en Provence

----------------------------------------------------------------------------

Préparation de l'environnement : 

* Créer un groupe de ressources
* Créer un workspace log analytics
* Si ce n'est pas déjà fait, mettre à niveau Azure Security Center vers la version standard
* Configurer la Security Policy - Data Collection - pour ce Workspace sur le niveau Common (afinde collecter les journaux de sécurité sur les serveurs Windows)
* Contrôler que la la Security Policy - Data Collection pour votre souscription est bien configurée en Auto Provisioning (afin que le monitoring agent soit automatiquement déployé au sein des VMs)
* Créer deux VMs Windows Server 2012 R2 type Standard B1s (1 vcpus, 1 GB memory)
* Une fois créer, vérifier que les deux VMs sont bien prises en compte dans Azure Security Center



----------------------------------------------------------------------------

# Utilisation d'Azure Monitor :

* Accéder au service Azure Monitor
* Parcourir les différents fonctonnalités
* Cliquer sur virtual machine dans la zone Insights et vérifier que les VMs sont monitorées (cela peut prendre un certain temps suite à leur déploiement)

Détection d'un évènement
* Lancer la connexion à une VMs
* Saisir plusieurs fois un mauvais mot de passe
* Dans azure Monitor, cliquer sur Logs
* Parcourir le schéma de votre workspace
* Dérouler la zone Security
* faire un double clic sur SecurityEvent (cela créer la première requete) puis cliquer sur RUN
* une liste d'evenements Securité doit apparaitre en résultats. ils ont été générés par les erruers de saisie de mote de passe (la détection d'evt peut prendre plusieurs minutes)
* Saisir la requete suivante : SecurityEvent |where EventID == 4625 afin de filtrer sur l'event ID 4625
* Enregistrer la requete
* Créer une alerte afin de vous envoyer un SMS



----------------------------------------------------------------------------

# Monitoring d'un site web

With Azure Monitor Application Insights,  
you can easily monitor your website for availability,  
performance, and usage. You can also quickly identify  
and diagnose errors in your application without waiting  
for a user to report them.  
Application Insights provides both server-side monitoring  
as well as client/browser-side monitoring capabilities.

<https://docs.microsoft.com/fr-fr/azure/azure-monitor/app/website-monitoring>


-------------------------------------------------------------------------------------

# Utilisation d'Azure Security center pour détecter des menaces

In this exercise, you will: 
* Demonstrate how to use built in Windows tools to download test malware and execute a suspicious process. 
* Demonstrate how Security Center detects those attacks 
* Demonstrate how Security Center creates a Security Incident based on data correlation 

<https://gallery.technet.microsoft.com/Azure-Security-Center-f621a046>

