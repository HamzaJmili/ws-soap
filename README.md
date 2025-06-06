# Projet de Service Web SOAP Banque

Un projet démonstratif pour mettre en œuvre et tester des services web SOAP en utilisant Jakarta EE (JAX-WS) pour un système bancaire simple.

---

## Table des matières

- [Introduction](#introduction)
- [Fonctionnalités](#fonctionnalites)
- [Technologies utilisées](#technologies-utilisees)
- [Structure du projet](#structure-du-projet)
- [Tests](#tests)
- [Captures d'écran](#captures-decran)

---

## introduction

Ce projet fait partie du programme Master SDIA, dans le cadre du cours *Systèmes Distribués et Middleware*. Il implémente un service web SOAP simple pour des opérations bancaires (gestion de comptes et conversion de devises) en utilisant Jakarta EE et JAX-WS.

---

## Fonctionnalités

- Conversion de devise (Euro en Dirham)
- Récupération d’un compte à partir de son code
- Liste de tous les comptes
- Publication des points d’accès SOAP via Jakarta EE (JAX-WS)
- Application cliente pour consommer le service web





## technologies utilisées

- Java 21+
- Jakarta EE (JAX-WS 4.x)
- Maven
- Metro JAX-WS RI
- IntelliJ IDEA

---

## Structure du projet

- `ma/service/Compte.java`: Account entity (JavaBean)
- `ma/service/BanqueService.java`: Web service implementation
- `ma/server/ServerJWS.java`: Publishes the web service
- `ma/proxy/`: Generated client proxy classes
- `ma/client/ClientWS.java`: Client application

---


## Tests
L'application cliente (ClientWS) permet de tester :

- La conversion de devise

- La récupération d’un compte par son code

- L’affichage de la liste des comptes

### Test avec SoapUI
Vous pouvez également tester les services SOAP avec SoapUI :

1.Démarrez le serveur (ServerJWS).

2.Ouvrez SoapUI et créez un nouveau projet SOAP.

3.Entrez l’URL WSDL :
http://localhost:8080/BanqueWS?wsdl

4.SoapUI générera les requêtes pour chaque opération disponible.

5.Testez les fonctions suivantes :

-convert : Saisir un montant en Euro pour obtenir l’équivalent en Dirham.

-getCompte : Fournir un code de compte pour récupérer ses détails.

-listComptes : Obtenir la liste complète des comptes.

Consultez les requêtes/réponses SOAP dans SoapUI pour valider le fonctionnement.
---
## Screenshots
### SoapUI
#### ConversionEuroToDH
![Screenshot 2025-05-24 172653](https://github.com/user-attachments/assets/75b709bd-d39a-4c5d-a07b-19fc08fa59d5)
#### GetCompte
![Screenshot 2025-05-24 172727](https://github.com/user-attachments/assets/90c8cfda-afa4-41ec-a785-55eb7fc477bd)
#### ListComptes
![Screenshot 2025-05-24 172807](https://github.com/user-attachments/assets/44afcb18-6f19-495b-957c-1f8495fbb2fd)
### Projet 
#### fichier xml wsdl
![Screenshot 2025-05-31 103716](https://github.com/user-attachments/assets/e68bc420-7fac-4a94-9f68-74e42c55a361)
#### Liste des comptes  
![Screenshot 2025-05-31 105813](https://github.com/user-attachments/assets/ab0b4918-c1f5-4fe7-976e-369cc1270066)
#### création le nouveau module dans le projet client-soap-java
![Screenshot 2025-05-31 110159](https://github.com/user-attachments/assets/dd3c1a9d-5d6d-4794-b756-a17b16cdfac3)





