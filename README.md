# Projet SAE – Piloter un projet informatique (Méthode Agile)

## Objectif du projet

Ce projet a pour but de mettre en place une architecture réseau complète sous **Cisco Packet Tracer**, comprenant :

- Deux réseaux locaux (Site A et Site B)
- Deux routeurs jouant le rôle de relais DHCP
- Un serveur DHCP principal
- Un pare-feu (Firewall) entre les deux réseaux
- Deux switches par site
- Un routeur simulant l’accès Internet
- Une séparation managers / employés via quatre VLAN

Le tout est géré selon la **méthodologie Agile**, avec une gestion de versions Git et un suivi Trello.

## Équipe de projet

**Lead Dev :** Nour Bensoltana
Responsable du dépôt Git, de la structure, et de l’intégration finale.

**Scrum Master :** Hiba Ben Younes
Responsable du tableau Trello, de l’organisation et des réunions.

**Membres :** Lisan SRITHARAN et Awa Salif DOUMBIA

## Structure du dépôt

SAE-Project-Agility/

- configs/
  - firewall/ – configuration du pare-feu intersite
  - routers/ – configurations des routeurs des sites et du WAN
  - serveurs/ – configurations des serveurs DHCP et WAN
  - switchs/ – configurations switchs des sites 

- simulation/
  - Topologie Packet Tracer complète (.pkt)

- README.md

## Fonctionnement du réseau

- VLAN 10 (Site A) et VLAN 30 (Site B) → Managers  
  - Communication managers ↔ managers autorisée (même site + intersite)  
  - Accès autorisé vers les employés du même site  

- VLAN 20 (Site A) et VLAN 40 (Site B) → Employés  
  - Accès autorisé uniquement vers les managers du même site  
  - Communication employés ↔ employés interdite  
  - Communication employés ↔ managers du site opposé interdite  

- ACL intersites pour contrôler les flux entre les sites  
- Filtrage Internet :  
  - HTTP, HTTPS, DNS, ICMP echo autorisés en sortie  
  - Connexions "established" autorisées en entrée  
  - ICMP echo-reply autorisé  
  - Tout autre trafic entrant bloqué  

- NAT Overload activé sur l'interface Internet  
- DHCP centralisé via le serveur WAN
