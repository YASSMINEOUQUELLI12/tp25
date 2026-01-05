# TP25 – Docker, Microservices & Consul

Ce lab montre comment conteneuriser une petite architecture **microservices Spring Boot** avec **Docker** et **Docker Compose**, et utiliser **Consul** comme service discovery.

---

## 🎯 Objectifs du lab

À la fin de ce lab, vous serez capable de :

- Expliquer pourquoi **Docker** est utile dans une architecture microservices.
- Créer un **Dockerfile multi-stage** pour un microservice Spring Boot.
- Orchestrer plusieurs conteneurs (MySQL, Consul, Gateway, Client, Voiture, phpMyAdmin) via **Docker Compose**.
- Comprendre la différence entre **localhost (machine hôte)** et les **noms DNS Docker** (`mysql`, `consul`, etc.).
- Vérifier l’enregistrement automatique des services dans **Consul**.
- Diagnostiquer les problèmes classiques : ports, réseau, base de données, dépendances, etc.

---

## 🧩 Scénario

Une petite architecture microservices est déjà fournie :

- **Service Client** (consomme le service Voiture via Gateway)
- **Service Voiture**
- **Gateway** (API Gateway)
- **MySQL** (base de données)
- **Consul** (service discovery)
- **phpMyAdmin** (interface de gestion MySQL)

En mode “classique”, chaque service est démarré à la main, avec des ports et des configurations à gérer.  
Dans ce lab, **un seul `docker-compose up`** permet de lancer toute l’architecture.

---

## ✅ Prérequis

### Outils à installer

- Docker
- Docker Compose
- Maven (optionnel, pour compiler localement)

### Vérifications (dans un terminal)

```bash
docker --version
docker compose version
mvn -version      # optionnel



<img width="1918" height="1018" alt="image" src="https://github.com/user-attachments/assets/a07f11b3-0229-46c2-a53c-5bdd10a61797" />

