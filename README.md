# 🚀 MinIO-CI-CD-Pipeline

A lightweight, self-hosted **CI/CD pipeline** for automated software deployment using **PowerShell**, **Python**, and **MinIO (S3-compatible storage)**.  
It automatically detects new builds, versions them, uploads to MinIO, and updates client systems safely — all without Jenkins or GitLab.

> 🧠 **Developed as part of a self-hosted CI/CD automation system demonstration for distributed software deployment.**

---

## 🧩 Overview

This system automates the deployment of software builds across client systems using MinIO as the central artifact repository.

- 🖥 **Server (PowerShell Watcher)** — detects new builds, versions them, uploads to MinIO, and updates version manifests.  
- 💻 **Client (Python Updater)** — checks for new versions, downloads updates, stops the running service, overwrites old files, and restarts automatically.  
- 🗂 **MinIO Storage** — hosts build artifacts, manifests, and version indexes.

---

## ⚙️ System Flow

[ Developer Builds App ]
↓
[ PowerShell Watcher ] → [ MinIO Server ] → [ Python Updater ] → [ Application Service ]


---

## 🪄 Usage

### 🖥 Server
1. Place your new build ZIP in the watch folder (e.g., `C:\dropbox`).
2. Run `watcher.ps1` — it uploads and versions the build automatically.

### 💻 Client
1. Run `python updater.py` to install the latest version.
2. Use `python updater.py --manual` for rollback or version selection.

---

## 👨‍💻 Author

**Gagan Chaudhary**  
Electronics & Communication Engineering (ECE)  
GL Bajaj Institute of Technology & Management
