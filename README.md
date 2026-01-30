# Docker Compose – Inter‑Container Messaging (Python)

## Overview

This project demonstrates the use of **Docker Compose** to coordinate multiple containers and pass a message between them before printing it to standard output.

The goal of the task is to ensure that the message:

> **"Nobody expects the Spanish Inquisition!"**

**travels between at least two containers** before being output, showcasing inter‑container communication using Docker Compose.

---

## Key Requirements (Satisfied)

* ✅ Uses **Docker Compose**
* ✅ Involves **multiple containers**
* ✅ Message passes **between containers** before being printed
* ✅ No changes made to the provided **Makefile**
* ✅ Solution works with the provided test workflow

---

## How It Works (High Level)

* One container is responsible for **producing or sending** the message.
* Another container **receives, processes, or forwards** the message.
* The message is transferred between containers using Docker networking.
* After passing through the containers, the message is written to **standard output**, where it is validated by the test script.

This approach goes beyond a single‑container print and demonstrates meaningful container interaction.

---

## Tech Stack

* **Python** – application logic
* **Docker** – containerisation
* **Docker Compose** – multi‑container orchestration
* **Bash** – automated testing (provided)

---

## How to Run

The project is controlled entirely via the provided Makefile.

```bash
make up      # start the Docker Compose setup
make test    # run the test script (./test.bash)
make stop    # stop and clean up containers
```

Expected output from `make test` (loosely):

```text
Nobody expects the Spanish Inquisition!
```

---

## Notes

* All required configuration and scripts are included in the repository.
* Any additional files required for the solution are tracked in Git.
* Docker Compose handles container startup order and networking.

---

## Purpose

This project was completed as part of a Docker learning exercise, with a focus on:

* Multi‑container architectures
* Inter‑container communication
* Clean, testable Docker Compose setups

---

## Author

Jabbar Oguntola
