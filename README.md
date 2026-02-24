# Dockerized WordPress Lab

A clean multi-container WordPress environment built with Docker Compose.

This project demonstrates how to deploy a containerized web stack for learning and practicing DevOps and System Administration concepts.

---

## Stack Overview

- WordPress (Apache + PHP)
- MySQL database
- phpMyAdmin
- Adminer
- Docker internal networking
- Persistent volumes
- Environment-based configuration using `.env`

---

## Project Structure

The repository separates configuration, environment variables, and persistent data:

- docker-compose.yaml  
  Defines services, networking, volumes, and environment bindings.

- .env  
  Stores sensitive configuration such as database credentials (not committed).

- .gitignore  
  Excludes runtime data and sensitive files from version control.

- mysql/  
  Persistent data directory for MySQL.

- wordpress/  
  WordPress files mounted into the container.

- README.md  
  Project documentation.

---

## Start the Stack

Run all services in detached mode:

```bash
docker compose up -d

## Service Endpoints

Once running, services are available at:

WordPress → http://127.0.0.1

phpMyAdmin → http://127.0.0.1:8000

Adminer → http://127.0.0.1:8080

## Stop the Stack

```bash
docker compose down
