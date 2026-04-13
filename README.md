# Docker Lab: Containerizing a Three-Tier Application
**INET 4031 - Introductions to Systems**

This lab introduces Docker and Docker Compose by having you containerize a
real, multi-service application. You will package three components: Apache,
Flask, and MariaDB. These will be packaged into separate containers and wired together so they function as a complete application.

The application code and scaffolding are provided. Your job is to complete the Dockerfiles, verify the stack runs correctly, and document your work below.

> **Directions and explanations for this lab are on the repository Wiki.**
> Refer to the Wiki pages for step-by-step instructions.

---

*The sections below are for you to fill out. Replace each placeholder with your own content before submitting. Having a detailed README is the best practice for showing your work in future GitHub repositories.*

---

# Project Overview

# Docker Lab: Containerizing a Three-Tier Application  
INET 4031 - Introduction to Systems  

## Project Overview
This project demonstrates how to containerize a three-tier application using Docker and Docker Compose. The application consists of three services: Apache, Flask, and MariaDB. These services are built into separate containers and connected through a shared Docker network to function as a complete ticket management system.

---


# Prerequisites

- Ubuntu VM 
- Docker and Docker Compose installed
- Git installed
- VS Code with Remote-SSH

# Getting Started


1. Clone the repository:
   git clone <your-repo-link>
   cd inet4031-testlab12

2. Create the Environment - cp .env.example .env

3. Build and Start the Containers using - sudo docker-compose up --build -d

4. Veriy containers using docker compose ps

5. Open a browser and go to your vm IP

# Configuration

The `.env` file contains environment variables used by both the database and Flask application. It is not included in the repository, so a teammate must create it from `.env.example` and provide values such as the database name, username, and passwords. These values must be consistent across services so the application can connect to the database correctly.

# Verification

The stack can be verified by checking that all containers are running (`docker compose ps`), confirming the dashboard loads in a browser with a healthy API indicator, and testing endpoints using curl. Running `./check-lab.sh` should result in all checks passing, confirming the application is functioning properly.
