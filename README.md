![Docker Web Application Architecture](https://image.noelshack.com/fichiers/2024/35/4/1724931574-mario-serveur.png)

# Softy Pinko Docker Project

## Table of Contents
- [Introduction](#introduction)
- [Project Structure](#project-structure)
- [How to Run the Project](#how-to-run-the-project)
- [Tasks Overview](#tasks-overview)
- [Scaling the Backend](#scaling-the-backend)
- [Useful Commands](#useful-commands)
- [Authors](#authors)

## Introduction

This project is a Docker-based deployment of the Softy Pinko static website along with a simple Flask API. The purpose of this project is to demonstrate the use of Docker containers to run both static and dynamic content, as well as to scale the backend API horizontally using Nginx as a load balancer.

Ce projet consiste en un déploiement basé sur Docker du site Web statique Softy Pinko, accompagné d'une API Flask simple. L'objectif de ce projet est de démontrer l'utilisation de conteneurs Docker pour exécuter du contenu statique et dynamique, ainsi que de mettre à l'échelle l'API backend de manière horizontale en utilisant Nginx comme équilibrage de charge.

## Project Structure

The project is divided into multiple tasks, each of which adds new features or improvements to the overall Docker configuration.

Le projet est divisé en plusieurs tâches, chacune ajoutant de nouvelles fonctionnalités ou améliorations à la configuration Docker globale.

```
holbertonschool-softy-pinko-docker/
├── task0/
├── task1/
├── task2/
├── task3/
├── task4/
├── task5/
└── task6/
```

- **front-end/**: Contains the Nginx configuration and static files for the front-end.
- **back-end/**: Contains the Flask API and its dependencies.
- **proxy/**: Contains the Nginx configuration for load balancing between multiple backend servers.

## How to Run the Project

1. **Clone the Repository**
   ```bash
   git clone https://github.com/your-username/holbertonschool-softy-pinko-docker.git
   cd holbertonschool-softy-pinko-docker
   ```

2. **Navigate to the Desired Task Directory**
   ```bash
   cd task6
   ```

3. **Build and Run the Containers**
   ```bash
   docker-compose up --build
   ```

4. **Access the Application**
   - Front-end: Open your browser and go to `http://localhost:9000`
   - API (via proxy): Go to `http://localhost/api/hello`

## Tasks Overview

- **Task 0:** Initial setup of the project structure and basic Docker configurations.
- **Task 1:** Adding the front-end server and setting up Nginx.
- **Task 2:** Introducing the Flask API as a back-end service.
- **Task 3:** Connecting the front-end with the back-end API.
- **Task 4:** Implementing a reverse proxy with Nginx.
- **Task 5:** Consolidating all configurations and preparing for deployment.
- **Task 6:** Scaling the back-end service horizontally.

## Scaling the Backend

In task 6, we scale the backend by running two instances of the Flask API. Nginx acts as a load balancer using the round-robin algorithm to distribute requests evenly between these instances.

Dans la tâche 6, nous mettons à l'échelle le backend en exécutant deux instances de l'API Flask. Nginx agit en tant qu'équilibreur de charge en utilisant l'algorithme round-robin pour distribuer les requêtes de manière égale entre ces instances.

## Useful Commands

- **Start the services:**
  ```bash
  docker-compose up
  ```

- **Stop the services:**
  ```bash
  docker-compose down
  ```

- **Scale the back-end:**
  ```bash
  docker-compose up --scale back-end=2
  ```

## Authors

- JHMindSharp
