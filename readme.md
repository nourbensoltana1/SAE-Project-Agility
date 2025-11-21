# Projet SAE – Piloter un projet informatique (Méthode Agile)

## Objectif du projet
Ce projet a pour but de mettre en place une architecture réseau complète sous **Cisco Packet Tracer**, comprenant :
- Deux réseaux locaux (LAN A et LAN B)
- Deux routeurs jouant le rôle de relais  DHCP
- un serveur dhcp principale
- Un pare-feu (Firewall) entre les deux réseaux
- 4 switchs
- un routeur

Le tout est géré selon la **méthodologie Agile**, avec une gestion de versions Git et un suivi Trello.

## Équipe de projet
- **Lead Dev :** Nour Ben Soltana
  Responsable du dépôt Git, de la structure, et de l’intégration finale.  
- **Scrum Master :** Hiba Ben Younes 
  Responsable du tableau Trello, de l’organisation et des réunions.  
- **Membres :** Awa Salif DOUMBIA et Lisan SRITHARAN

## Structure du dépôt
SAE-Project-Agility/
├── README.md
├── .gitignore
├── packet-tracer/
├── configs/
├── docs/
│ └── sprints/
└── tests/

##  Méthodologie Agile
- Chaque membre travaille sur une **branche dédiée** :
  - `feature/dhcp` → configuration DHCP et routage
  - `feature/vlans` → configuration vlan  
  - `feature/firewall` → configuration du pare-feu  
  - `feature/nat` → traduction d’adresses (NAT)  
  - `feature/docs` → documentation et rapports
- Les validations intermédiaires sont intégrées dans `develop`.
- La version finale est fusionnée dans `main`.

##  Livrables attendus
- Fichiers Packet Tracer `.pkt`
- Sauvegardes de configuration (`.cfg`)
- Documentation complète (`plan_adressage.md`, schémas, tests)
- Historique Git clair avec commits en français
